<template>
    <section>
        <ul>
<!--            데이터 바인딩은 {{}} 혹은 v-bind 이용-->
            <li v-for="todoItem in todoItems" v-bind:key="todoItem">{{ todoItem }}</li>
        </ul>
    </section>
</template>

<script>
    export default {
        data() {
            return {
                todoItems: []
            }
        },
        created() {
            if (localStorage.length > 0) {
                for (var i = 0; i < localStorage.length; i++) {
                    this.todoItems.push(localStorage.key(i));
                }
            }
        }

    }
</script>

<style scoped>

</style>