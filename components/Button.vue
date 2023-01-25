<template>
  <div class="containerBtn">
        <img v-if="icon == 'income'" src="../assets/images/income.png"/>
        <img v-else src="../assets/images/spending.png" />
        {{  text }}
  </div>
</template>
<script>
export default {
  name: "ButtonApp",
  props: {
    icon: String,
    text: String
  },
}
</script>
<style scoped>
.containerBtn{
    display: flex;
    flex-direction: row;
    justify-content: center;
    width: 100%;
    align-items: center;
}
.btn{
    background-color: var(--bg-btn);
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    white-space: nowrap;
    width: 100%;

}
</style>
