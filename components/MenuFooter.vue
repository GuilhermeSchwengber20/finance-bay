<template>
  <div class="containerItem">
    <div :id="`menu-${idx}`" class="item" v-for="(item, idx) in menu" :key="idx" @click="setSelected(item, idx)" >
      <nuxt-link :to="`${item.to}`" class="link">
        <div>
          <img :src="item.img" />
        </div>
        <span v-if="item.active">{{ item.title }}</span>
      </nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "FooterMenu",
  props: { 
    selectedItem: Object, 
    index: Number 
  },
  data() {
    return {
      menu: [

      
        {
          title: "My Budget",
          img: require("../assets/images/wallet.png"),
          to: "budget",

        },
        {
          title: "My Plans",
          img: require("../assets/images/plans.png"),
          to: "plans",

        },
        {
          title: "My Graphs",
          img: require("../assets/images/graph.png"),
          to: "graphs",

        },
        {
          title: "Transfers",
          img: require("../assets/images/transactions.png"),
          to: "transfers"
        },
      ]
    }
  },
  mounted(){
    if(this.selectedItem){
      this.setSelected(this.selectedItem, this.index)
    }
  },
  methods: {
    setSelected(item, idx){
      const menuSelected = document.getElementById(`menu-${idx}`);
      // QUANDO SELECIONAR O MENU E TROCAR DE PAGE
      if(this.selectedItem){
        const itemProp = this.menu.find(element => element.title == item.title);
        if(itemProp){
          itemProp.active = true;
        }
      }
      if(item.active){
        return;
      }
      // this.menu.forEach((item, index) => {
      //   if(index != idx){
      //     const element = document.getElementById(`menu-${index}`);
      //     element?.classList.remove("selected");
      //     item.active = false;
      //     this.$forceUpdate();
      //   }
      // });
      menuSelected.classList.add("selected");

      this.$forceUpdate();
    }
  }
}
</script>
<style scoped>
.containerItem {
  position: absolute;
  bottom: 0px;
  width: 100%;
  padding: 5px 0px;
  display: flex;
  flex-direction: row;
  justify-content: center;
  gap: 40px;
  background-color: #FFF;
}

.item{
  display: flex;
  flex-direction: row;
  white-space: nowrap;
  align-items: center;
  justify-content: center;
}

.item span{
  font-weight: 600;
  margin-left: 3px;
  font-size: 1.1rem;
}

.item img {
  width: 35px;
}

.link{
  text-decoration: none;
  color: #000;
  display: flex;
  flex-direction: row;
  align-items: center;

}

.selected {
  background-color: var(--arrow);
  padding: 5px 5px;
  border-radius: 10px;
}
</style>
