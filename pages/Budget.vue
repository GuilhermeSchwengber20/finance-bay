<template>
  <div class="containerPage">
    <div class="containerHeader">
        <h2>Hello, Joshephine</h2>
        <span>Here you can view overview of yout budget</span>
    </div>
    <MyBudget />
  </div>
</template>
<script>
export default {
  name: "Budget",
}
</script>
<style scoped>
.containerPage{
  height: 100vh;
}

.containerHeader h2{
  font-size: 2rem;
}

.containerHeader span{
  font-size: 1rem;
  color: var(--arrow)
}

</style>
