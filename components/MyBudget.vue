<template>
    <div class="budgetContainer">
        <div class="budgetContent">
            <span>My Budget</span>
            <h2>
                R$ 1550,00 
                <!-- TROCAR PARA VARIAVEL DINAMICA FUTURAMENTE -->
            </h2>
            <div>
                <Button :text="'Add Income'" :icon="'income'"/>
                <Button :text="'Add Spending'" :icon="'speding'"/>
            </div>
        </div>
        <div class="budgetOverview">

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
    height: 20vh;
    background-color: var(--bg);
    border-radius: 20px;
}

.budgetContent{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 15px 0px;
}
.budgetContent div{
    display: flex;
    flex-direction: row;
    width: 100%;
}
.budgetContent span{
    font-weight: 500;
    font-size: 1.2rem;
    margin-bottom: 10px;
}
.budgetContent h2{
    font-size: 1.5rem;
}
</style>