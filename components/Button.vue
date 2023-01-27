<template>
  <div class="btn">
        <img v-if="icon == 'income'" src="../assets/images/income.png"/>
        <img v-else src="../assets/images/spending.png" />
        &nbsp;
        <span>{{  text }}</span>
        
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
.btn{
  background-color: var(--bg-btn);
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  white-space: nowrap;
  width: 50%;
  padding: 5px 10px;
  border-radius: 20px;
}
.btn span{
  font-weight: 600;
}
</style>
