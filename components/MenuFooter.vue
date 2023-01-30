<template>
  <div class="containerItem">
    <div id="my-budget" class="item" @click="setSelected('my-budget')">
      <img src="../assets/images/wallet.png" />
      <span v-if="span === 'my-budget'">My budget</span>
    </div>
    <div id="my-plans" class="item" @click="setSelected('my-plans')">
      <img src="../assets/images/plans.jpg" />
      <span v-if="span === 'my-plans'">My plans</span>
    </div>
    <div id="my-transactions" class="item" @click="setSelected('my-transactions')">
      <nuxt-link to="/transactions">
        <img src="../assets/images/transacao.png" />
      <span v-if="span === 'my-transactions'">My transactions</span>
      </nuxt-link>
    </div>
  </div>
</template>
<script>
export default {
  name: "FooterMenu",
  data() {
    return {
      span: "",
    }
  },
  methods: {
    setSelected(id) {
      console.log(this.$route);
    },
  },
}
</script>
<style scoped>
.containerItem {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  padding: 0px 20px;
  gap: 50px;
}

.item img {
  width: 30px;
}

.item.selected {
  background-color: #cecece;
}
</style>
