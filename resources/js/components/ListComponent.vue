<template>
    <ul class="list">
        <li v-for="(item, index) in listdata" :key="index">
        {{item.title}} 
        <button-form text="Hapus" class="delete" @emitClick="deleteList"/>
        </li>
    </ul>
</template>

<script>
import ButtonComponent from './ButtonComponent.vue'
export default {
    components: { ButtonComponent },
    props:{
        listdata:{
            type: Array,
            default: () => {
                return []
            }
        }
    },
    methods: {
        deleteList(index) {
            this.$emit('emitDelete', index)
        }
    }
}
</script>