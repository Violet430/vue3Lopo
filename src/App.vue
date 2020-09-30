<template>
<img alt="Vue logo" src="./assets/logo.png" />
<HelloWorld msg="Welcome to Your Vue.js App" />
<TodoList />
<Footer />
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Footer from "./components/Footer.vue";
import TodoList from "./components/TodoList.vue";

export default {
    name: "App",
    components: {
        HelloWorld,
        Footer,
        TodoList,
    },
};
</script>

<style>
#app {
    background-color: rgb(245, 245, 220);
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
}
</style>
