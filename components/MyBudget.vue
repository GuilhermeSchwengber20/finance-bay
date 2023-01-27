<template>
    <div class="budgetContainer">
        <div class="budgetContent">
            <span>My Budget</span>
            <h2>
                R$ 1550,00 
                <!-- TROCAR PARA VARIAVEL DINAMICA FUTURAMENTE -->
            </h2>
            <div class="containerBtn">
                <Button :text="'Add Income'" :icon="'income'"/>
                <Button :text="'Add Spending'" :icon="'spending'"/>
            </div>
        </div>
        <div class="line"></div>
        <div class="budgetOverview">
            <span>Budget overview</span>
            <div class="cardContainer">
                <CardOverview :type="'income'"/>
                <CardOverview :type="'spending'"/>
            </div>
        </div>
    </div>
</template>
<style scoped>
.budgetContainer{
    width: 90%;
    margin: 20px auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    height: auto;
    background-color: var(--bg);
    border-radius: 20px;
}

.budgetContent{
    display: flex;
    width: 90%;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 15px 0px;
}

.budgetContent span{
    font-weight: 500;
    font-size: 1.2rem;
    margin-bottom: 10px;
}
.budgetContent h2{
    font-size: 1.5rem;
}

.containerBtn{
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-top: 15px;
}
.line{
    width: 95%;
    height: 1px;
    background-color: var(--bg-btn);
    margin-bottom: 10px;
}
.budgetOverview{
    width: 100%;
    padding: 5px 10px;
}
.budgetOverview span{
    font-weight: 600;
    font-size: 1rem;
}
.cardContainer{
    width: 100%;
    display: flex;
    flex-direction: row;
    gap: 15px;
}
</style>