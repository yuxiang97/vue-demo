<template>
    <div class="todo-container">
        <ol>
            <li v-for="(item, index) in todos" :key="index">{{ item }}</li>
        </ol>
        <div class="input">
            <input type="text" v-model="item">
            <button v-on:click="submitTodo">提交</button>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Todo",
        data(){
            return {
                todos:[
                    'xuexi',
                    'youxi'
            ],
                item:''
            }
        },
        methods:{
            submitTodo(){
                if(this.item !== '') {
                    this.todos = [...this.todos,this.item]
                    this.item = ''
                } else {
                    alert('名称不能为空')
                }
            }
        }
    }
</script>

<style>

</style>
