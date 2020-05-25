<template>
    <div>
        <h1>Lotto</h1>
        <button @click="creatNumber">숫자생성</button>
        <p>{{ lucky }}</p>
    </div>
</template>

<script>
var _ = require('lodash');
export default {
    data: function(){
        return {
            numbers: _.range(1,46),
            lucky: '',
        }
    },
    methods: {
        creatNumber(){
            this.lucky = _.sampleSize(this.numbers, 6)
        }
    }
}
</script>

<style>

</style>