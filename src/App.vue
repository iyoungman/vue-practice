<template>
    <div id="app">
        <TodoHeader></TodoHeader>
        <TodoInput></TodoInput>
        <TodoList></TodoList>
        <TodoFooter></TodoFooter>
    </div>
</template>

<script>
    import TodoHeader from "@/components/TodoHeader";
    import TodoFooter from "@/components/TodoFooter";
    import TodoList from "@/components/TodoList";
    import TodoInput from "@/components/TodoInput";

    //각 컴포넌트를 등록하기 위해 최상위 컴포넌트에 등록
    export default {
        components: {
            //이름 : 컴포넌트 이름
            'TodoHeader': TodoHeader,
            'TodoInput': TodoInput,
            'TodoList': TodoList,
            'TodoFooter': TodoFooter
        }
    }
</script>

<style>
    body {
        text-align: center;
        background-color:blanchedalmond;
    }
    input {
        border-style: groove;
        width: 200px;
    }
    button {
        border-style: groove;
    }
</style>
