<template>
    <div class="container">
        <h1>test saja</h1>
        <input-form @emitSubmit="addList"/>
        <list :listdata="list" @emitDelete="deleteList"/> 
    </div>
</template>

<script>

    export default {
        data(){
            return{
                list: [
                    {
                        title: "menyapu"
                    },
                    {
                        title: "cuci piring"
                    }
                ],
                input: ""
            }
        },
        methods:{
            addList(data) {
                let newList = {
                    title: data
                }
                this.list.push(newList)
                // this.input = ""
            },
            deleteList(index) {
                this.list.splice(index, 1)
            }
        }
    }

</script>