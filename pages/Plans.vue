<template>
    <div class="containerPage">
        <div class="contentPage">
          sadasdas
        </div>
        <div class="footer">
          <MenuFooter :selectedItem="{title: 'My Plans'}" :index="1"/>
        </div>
    </div>
</template>
<script>
export default {
  name: "Plans",
}
</script>
<style scoped>
.containerPage{
  height: 100vh;
  overflow: none;
}
.contentPage{
  height: 80vh;

}
</style>
