<template>
    <ul class="todo-main">
        <MyItem v-for="todo in todos" :key="todo.id" :todo="todo" />
    </ul>
</template>

<script>
    import MyItem from './MyItem.vue'
    export default {
        name: 'MyList',
        data() {
            return {
                todos: [{
                        id: '001',
                        title: '打代码',
                        done: false
                    },
                    {
                        id: '002',
                        title: '睡觉',
                        done: true
                    },
                    {
                        id: '003',
                        title: '吃饭',
                        done: false
                    }
                ]
            }
        },
        components: {
            MyItem
        }
    }
</script>

<style scoped>
    .todo-main {
        margin-left: 0;
        border: 1px solid #ddd;
        border-radius: 2px;
        padding: 0;
    }

    .todo-empty {
        height: 40px;
        line-height: 40px;
        border: 1px solid #ddd;
        border-radius: 2px;
        padding-left: 5px;
        margin-top: 10px;
    }
</style>