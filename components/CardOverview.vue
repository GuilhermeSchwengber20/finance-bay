<template>
  <div class="card">
    <div class="headerCard">
        <div class="containerImg">
            <img v-if="type == 'income'" src="../assets/images/income.png" />
            <img v-else src="../assets/images/spending.png" />
        </div>
        <div>
            <!-- Mudar para variavel futuramente -->
            <span v-if="type == 'income'" style="color: var(--income); font-weight: 600">+2,63%</span> 
            <span v-else style="color: var(--spending); font-weight: 600">-1,89%</span> 
        </div>
    </div>
    <div class="footerCard">
        <div class="containerPrice">
            <span v-if="type == 'income'" style="color: var(--arrow); font-weight: 600;">Incomes</span>
            <span v-else  style="color: var(--arrow); font-weight: 600;">Spending</span>
            <span class="price">$ 3.000,00</span>
        </div>
        <div class="containerIcon">

        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardOverview",
  props: { type: String },
}
</script>
<style scoped>
.card{
    margin-top: 10px;
    width: 60%;
    background-color: #FFF;
    height: 13vh;
    border-radius: 15px;
    padding: 5px 10px;
}

.containerImg{
    /* background-color: #000; */
    border-radius: 50%;
    width: 35px;
}

.headerCard{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
}
.footerCard{
    margin-top: 18%;
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
}
.containerPrice{
    display: flex;
    flex-direction: column;
}
.price{
    font-weight: 700;
    font-size: 1.1rem;
}
.containerIcon{
    width: 30px;
    height: 30px;
    border-radius: 50%;
    border: 1px solid black;
}
</style>
