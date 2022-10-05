<template>
    <button type="button" @click="buttonClick" :class="color">{{text}}</button>
</template>

<script>
export default {
    props:{
        text:{
            type: String,
            default: ""
        },
        color:{
            type: String,
            default: ""
        }
    },
    methods:{
        buttonClick(){
            this.$emit('emitClick')
        }
    }
}
</script>

<style scoped>
.transparent{
    font-size: 11px;
    color: darksalmon;
    background: transparent;
}
.blue{
    background: lightblue;
}
</style>

