<template>
  <div class="containerPage">
    <div class="containerHeader">
      <h2>Hello, Joshephine</h2>
      <span>Here you can view overview of yout budget</span>
    </div>
    <div class="wallet">
      <MyBudget />
    </div>
    <div class="plans">
      <MyPlan />
    </div>
    <div class="transactions">
      <MyTransactions />
    </div>
    <div class="footer">
      <MenuFooter :selectedItem="{title: 'My Budget'}" :index="0"/>
    </div>
  </div>
</template>
<script>
export default {
  name: "Budget",

  mounted(){
    window.addEventListener("wheel", (e) => {
      e.preventDefault();
    })
  }
}
</script>
<style scoped>
.containerPage{
  height: 93vh;
  overflow: none;
  background-color: #f7f7f7;
}

.wallet{
  height: 40vh;
}

.containerHeader h2{
  font-size: 2rem;
}

.containerHeader span{
  font-size: 1rem;
  color: var(--arrow)
}

</style>
