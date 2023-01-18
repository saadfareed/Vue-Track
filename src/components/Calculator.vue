<template>
    <div>
        <h1>Calculator</h1>
        <div class="form" ><input type="text" v-model="firstNumber">
        <input type="text" v-model="secondNumber"></div>
        <div class="fields"><button @click="add">Add</button>
        <button @click="subtract">Subtract</button>
        <button @click="multiply">Multiply</button>
        <button @click="divide">Divide</button></div>
        <div class="result"><p>Result: {{ result }}</p></div>
    </div>
  
</template>

<script>
export default {
    name: "CalculatorDisplay",
    data() {
        return {
            firstNumber: 0,
            secondNumber: 0,
            result: 0
        }
    },
    methods: {
        add() {0
            this.result = parseInt(this.firstNumber) + parseInt(this.secondNumber);
        },
        subtract() {
            this.result = parseInt(this.firstNumber) - parseInt(this.secondNumber);
        },
        multiply() {
            this.result = parseInt(this.firstNumber) * parseInt(this.secondNumber);
        },
        divide() {
            this.result = parseInt(this.firstNumber) / parseInt(this.secondNumber);
        }
    }

}
</script>

<style>
.form {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
}
.fields {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
}
.result {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    text-emphasis-color: rgb(255, 0, 0);
    color: rgb(255, 0, 0);
}

</style>