<template>
    <section class="section"> 
        <div class="content"> 
            <h1 class="title"> Todo App </h1> 
        </div> 
       
<div class="card">
        <todo-form></todo-form> 

        </div>
    
        <todo-filter></todo-filter>
        <todo-list></todo-list> 

              <div class="foot"> 
            <footer class="footer">Made with ❤️ by <a href="http://github.com/ayodelesalimon">Ayodele Salimonu</a>
            </footer>
            </div>
    </section>
 
</template>

<script>
import TodoForm from './TodoForm'
import TodoList from './TodoList'
import TodoFilter from './TodoFilter'

export default {
    name: 'TodoApp',
    components: {
        TodoForm,
        TodoList,
        TodoFilter
    }
}
</script>

<style scoped>
.section{
    padding: 10px;
}
.title{
    font-size: 30px;
    text-align: center;
   
}
.card{
    display: flex;
    justify-content: center;
}
.footer {
    
    text-align: center;
    font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
    font-size: 20px;
    color: black;
}
.footer a{
    text-decoration: none;
    color: rgb(33, 33, 214);
    
}
.foot{
   padding: 100px 250px;
}
</style>
