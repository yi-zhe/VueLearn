<template>
    <li>
        <label>
            <input type="checkbox" :checked="todo.done" />
            <span>{{todo.title}}</span>
        </label>
        <button class="btn btn-danger" style="display: none;">删除</button>
    </li>
</template>

<script>
    export default {
        name: 'MyItem',
        props: ['todo']
    }
</script>

<style scoped>
    li label {
        float: left;
        cursor: pointer;
    }

    li label li input {
        vertical-align: middle;
        margin-right: 6px;
        position: relative;
        top: -1px;
    }

    li button {
        float: right;
        display: none;
        margin-top: 3px;
    }

    li:before {
        content: initial
    }

    li:last-child {
        border-bottom: none;
    }
</style>