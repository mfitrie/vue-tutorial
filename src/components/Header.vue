<template>
    <header>
        <h1>{{title}}</h1>
        <Button @btn-click="$emit('toggle-add-task')" :text="showAddTask ? 'Close' : 'Add Task' " :color="showAddTask ? 'red' : 'green' "/>
        <!-- <Button text="Update Taskk" color="blue"/>
        <Button text="Delete Task" color="red"/> -->
    </header>
</template>


<script>
import Button from './Button.vue'

    export default {
        name: 'Header',
        // props: ['title'],
        // props: {
        //     title: {
        //         type: String,
        //         default: 'Hello World'
        //     }
        // },
        props: {
            title: String,
            showAddTask: Boolean
        },
        components: {
            Button
        }
    }
</script>


<!--style scope is only for this header-->
<style scoped>
    header{
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 20px;
    }
</style>