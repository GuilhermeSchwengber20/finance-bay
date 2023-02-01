<template>
  <div class="containerTrans">
    <div class="headerTrans">
      <div>
        <span>My transactions</span>
      </div>
      <div>
        <span>View all</span>
      </div>
    </div>
    <div class="bodyTransactions" >
        <CardTransaction :type="'income'"/>
        <CardTransaction :type="'income'"/>
    </div>
  </div>
</template>
<script>
export default {
  name: "MyTransactions",
}
</script>
<style scoped>
.containerTrans {
  width: 100%;
  height: 25vh;
  overflow-x: hidden;
}
.headerTrans {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 0px 25px;
  margin-bottom: 5px;
}
.headerTrans div:nth-child(1) span {
  font-size: 1.1rem;
  font-weight: 600;
}

.bodyTransactions{
    width: 90%;
    border-radius: 10px;
    margin: auto;
    background-color: #FFF;
    height: 25vh;
}

</style>
