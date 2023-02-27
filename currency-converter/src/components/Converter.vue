<template>
    <div class="converter">
        <h2>{{ currencyA }} to {{ currencyB }}</h2>
        <input type="text" v-model="currencyA_value" v-bind:placeholder="currencyA">
        <input type="button" value="Convert" v-on:click="convertUSDtoBRL">
        <h2>{{ currencyB_value }}</h2>
    </div>
</template>

<script>

export default {
    name: "Converter",
    props: ["currencyA", "currencyB"],
    data() {
        return {
            currencyA_value: "",
            currencyB_value: "0"
        };
    },
    methods: {
        convertUSDtoBRL() {
            let quotationUSDtoBRL = 5.19
            this.currencyB_value = (quotationUSDtoBRL * parseFloat(this.currencyA_value)).toFixed(2)
        }
    }
};
</script>

<style scoped>
.converter {
    max-width: 300px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    padding: 20px;

    background: radial-gradient(circle at 52.1% -29.6%, rgb(144, 17, 105) 0%, rgb(51, 0, 131) 100.2%);    
    color: rgb(255, 255, 255);
    border-radius: 10px;

    position: absolute;
    top:40%;
    left: 43%;
}
</style>