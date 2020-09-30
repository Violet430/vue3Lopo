<template>
<div class="todoList draggable">
    <div class="todoHeader">
        <span class="todoTitle">TodoList</span>
        <span class="todoMonth">12月</span>
        <span class="todoTime">星期日 21日 20:55</span>
        <div style="clear: both"></div>
    </div>
    <div class="todoTools" @click="todoListTools">
        <button class="toolButton">All</button>
        <button class="toolButton">Closed</button>
        <button class="toolButton">Open</button>
        <button class="toolButton">Add</button>
    </div>
    <div id="todoListContent" class="todoContent">
        <div id="sssss" class="test">
            <p>title</p><input class="myInput" placeholder="sddd" />
        </div>
        <div>78978979</div>
        <div>123132123</div>
        <div>78978979</div>
        <div>123132123</div>
        <div>78978979</div>
        <div>123132123</div>
        <div>78978979</div>
        <div>123132123</div>
        <div>78978979</div>
        <div>123132123</div>
    </div>
</div>
</template>

<script lang="ts">
export default {
    name: "TodoList",
    props: {},
    methods: {
        todoListTools(event) {
            if (event.target.tagName != "BUTTON") {
                return;
            }
            document.getElementById("sssss").style.display = "flex";
            document.getElementById("sssss").classList.add("slide-in-fwd-center");
            console.log("click!" + event.target.tagName);
        },
    },
};
</script>>

<style scoped>
.draggable {
    cursor: pointer;
}

.todoList {
    max-width: 98%;
    margin-right: 20px;
    --whiteShadow: -8px -8px 10px rgba(245, 245, 220, 0.63);
    --blackShadow: 8px 8px 10px rgba(78, 48, 48, 0.233);
    background: #355c7d;
    /* fallback for old browsers */
    background: -webkit-linear-gradient(to top, #c06c84, #6c5b7b, #355c7d);
    /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to top, #c06c84, #6c5b7b, #355c7d);
    /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */

    background-color: rgb(94, 179, 60);
    box-shadow: var(--blackShadow), var(--whiteShadow);
    width: 450px;
    height: 800px;
    border-radius: 30px;
    position: fixed;
    left: 20px;
    top: 50px;
}

.todoHeader {
    width: 100%;
}

.todoTime {
    font-family: Microsoft YaHei;
    font-weight: 300;
    font-size: 30px;
    margin-left: 40px;
    margin-top: 2px;
    color: white;
    float: left;
}

.todoTools {
    margin: 0 auto;
    width: 96%;
    height: 40px;
    background-color: white;
    border-radius: 30px;
    padding: 2px;
    display: flex;
    justify-content: space-around;
}

.todoContent {
    width: 100%;
    height: 580px;
    border-radius: 30px;
    overflow-y: overlay;
}

.toolButton {
    outline: none;
    text-align: center;
    line-height: 34px;
    vertical-align: middle;
    font-size: 20px;
    background-color: rgb(68, 150, 122);
    color: white;
    display: flex;
    float: left;
    width: calc(100% / 5);
    border-radius: 20px;
    height: 34px;
    margin: auto auto;
    border: 0px;
    cursor: pointer;
}

.myInput {
    outline: none;
    font-family: Microsoft YaHei;
    padding-left: 15px;
    text-align: left 10px;
    width: 90%;
    height: 35px;
    border: 2px solid gray;
    border-radius: 10px;
    font-size: 20px;
    line-height: 35px;
}

.myInput:focus {

    border: 2px solid rgb(94, 91, 91);
}

::-webkit-scrollbar {
    width: 8px;
    height: 10px;
}

::-webkit-scrollbar-thumb {
    margin-bottom: 10px;
    height: 3px;
    background-clip: padding-box;
    border-radius: 7px;
    background-color: rgba(255, 255, 255, 0.5);
}

::-webkit-scrollbar-button {
    width: 0;
    height: 0;
    display: none;
}

::-webkit-scrollbar-corner {
    background-color: transparent;
}

.test {
    display: none;
    width: 96%;
    margin: 0 auto;
    margin-top: 20px;
    height: 500px;
    background-color: rgb(117, 192, 139);
    border-radius: 30px;
    padding: 2px;
    position: relative;
}

.slide-in-fwd-center {
    -webkit-animation: slide-in-fwd-center 1.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
    animation: slide-in-fwd-center 1.5s cubic-bezier(0.25, 0.46, 0.45, 0.94);
}

@-webkit-keyframes slide-in-fwd-center {
    0% {
        -webkit-transform: translateZ(-1400px);
        transform: translateZ(-1400px);
        opacity: 0;
    }

    100% {
        -webkit-transform: translateZ(0);
        transform: translateZ(0);
        opacity: 1;
    }
}

@keyframes slide-in-fwd-center {
    0% {
        -webkit-transform: translateZ(-1400px);
        transform: translateZ(-1400px);
        opacity: 0;
    }

    100% {
        -webkit-transform: translateZ(0);
        transform: translateZ(0);
        opacity: 1;
    }
}

.toolButton:active {
    background-color: rgb(53, 128, 103);
}

.toolButton:focus {
    background-color: rgb(125, 211, 182);
}

.todoMonth {
    font-family: Microsoft YaHei;
    font-weight: 300;
    font-size: 70px;
    margin-right: 20px;
    margin-top: 60px;
    color: white;
    float: right;
}

.todoTitle {
    font-family: Microsoft YaHei;
    font-weight: 700;
    float: left;
    color: white;
    margin-left: 20px;
    margin-top: 20px;
    left: 0px;
    font-size: 60px;
}
</style>
