<template>
    <form class="form">
        <input type="text" v-model="inputform" />
        <button-form text="Reset"  @emitClick="reset"/>
        <button-form text="Submit" @emitClick="addList"/>
       
    </form>
</template>

<script>
import { emit } from 'process';

export default {
    data() {
        return{
            inputform: "",
        };
    },
    methods: {
        addList() {
            this.$emit("emitSubmit", this.inputform);
            this.inputform = ""
        },
        reset() {
            this.inputform = ""
        }
    },
};
</script>