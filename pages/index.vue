<template>
  <div>
    <Tutorial />
    <MenuFooter :selectedItem="{title: 'My Budget'}" :index="0"/>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  mounted(){
    window.addEventListener("wheel", (e) => {
      console.log(e);
      e.preventDefault();
    })
  }
}
</script>
