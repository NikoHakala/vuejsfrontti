<template>
    <div>
        <input type="desc" placeholder="Description" v-model="todos.description" />
        <input type="date" placeholder="Date" v-model="todos.date" />
        <button v-on:click="add">Add</button>
        <table>
            <tbody>
                <tr v-for="( todos, index ) in todoss" v-bind:key="index">
                    <td>{{ todos.description }}</td>

                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
export default {
    name: 'Todolist',
    data(){
        return{
            todos: [ todo:
                {description: ''},
                {date:''}
            ]
        }
    },   
    methods: {
        add: function(){
            this.todos.push(this.todos.description);
        
            this.todos.date='';
        }
    } 
}
</script>

<style scoped>
table {
    margin: auto;
}
</style>