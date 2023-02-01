<template>
  <div class="containerPlan">
    <div class="headerPlan">
      <div>
        <span>My plans</span>
      </div>
      <div>
        <span>View all</span>
      </div>
    </div>
    <div class="bodyPlan" id="containerPlan">
      <CardPlans />
      <CardPlans />
      <CardPlans />
      <CardPlans />
      <CardPlans />
      <CardPlans />
    </div>
  </div>
</template>
<script>

export default {
  name: "MyPlan",
  mounted(){
    this.carrouselEvent();
  },
  methods: {
    carrouselEvent(){
      const div = document.getElementById("containerPlan");
      div.addEventListener("touchstart", (e) => {
        console.log(e);
      })
    }
  },
}
</script>
<style scoped>
.containerPlan{
  width: 100%;
  height: 25vh;
  overflow-x: hidden;
}
.headerPlan{
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0px 25px;
}
.headerPlan div:nth-child(1) span{
  font-size: 1.1rem;
  font-weight: 600;
}

.bodyPlan{
  margin-top: 10px;
  width: 100%;
  overflow-x: auto;
  padding: 5px 25px;
  display: flex;
  flex-direction: row;
  gap: 10px;
  flex-wrap: nowrap;
}
</style>