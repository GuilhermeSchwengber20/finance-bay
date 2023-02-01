<template>
  <div class="containerCard">
    <div class="cardHeader">
        <div>
            <span id="category"># Category</span>
        </div>
        <div class="planTitleContainer">
            <span id="planTitle">Trip to Waduk Cengkik</span>
        </div>
    </div>
    <div class="cardBody">
        <div class="priceContainer">
            <div>
                <span id="obtainedVale">$249</span>
            </div>
            <div>
                <span id="finalValue">$400</span>
            </div>
        </div>
        <div class="bgProgress">
            <div class="progressbar">
                <div class="point"></div>
            </div>
        </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "CardPlans",
}
</script>
<style scoped>

.containerCard{
    min-width: 250px;
    padding: 10px;
    height: auto;
    background-color: #FFF;
    border-radius: 15px;
    box-shadow: 1px 1px 1px 1px black;
}

#category{
    color:blueviolet;
}

.planTitleContainer{
    margin-top: 3px;
}
#planTitle{
    font-size: 16px;
    font-weight: 700;
}
.priceContainer{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    padding: 10px 5px;
    margin-top: 18px;
}

#obtainedVale{
    font-weight: 700;
    font-size: 16px;
}
#finalValue{
    font-weight: 700;
    font-size: 16px;
    color: var(--arrow);
}

.bgProgress{
    background-color: #e6e6e6;
    width: 220px;
    height: 15px;
    margin: auto;
    border-radius: 15px;
}

.progressbar{
    width: 80%;
    background-color: blueviolet;
    height: 15px;
    border-radius: 15px;
    display: flex;
    flex-direction: row;


    justify-content: flex-end;
    align-items: center;
}

.point{
    width: 12px;
    height: 12px;
    background-color: #FFF;
    border-radius: 50%;
    margin-right: 3px;
}
</style>
