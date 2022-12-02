<template>
    <div>
        <div v-bind:key="todo.id" v-for="todo in todoslist">
            <div>{{todo.title}}</div>
        </div>
    </div>
</template>
<script>
    export default {
        name:'TodosWeb',
        props:['todoslist']
    }

</script>


<style></style>