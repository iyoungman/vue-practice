<template>
    <div>
        <input type="text" v-model="newTodoItem">
        <button v-on:click="addTodo">추가</button>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                newTodoItem: ''
            }
        },
        methods: {
            addTodo() {
                if(this.newTodoItem != "") {
                    var value = this.newTodoItem.trim();
                    localStorage.setItem(value, value);
                    this.clearInput();
                }
            },
            clearInput() {
                this.newTodoItem = "";
            }
        }
    }
</script>

<style scoped>

</style>