<template>
    <section>
       

        <div class="card" v-for="(todo, index) in todos" :key="index" >
            <div class="container" >
                <p>
                        {{ todo.text }}
                </p>
                <a  href="#"
                            v-show="!todo.done"
                            class="button is-pulled-right" 
                            @click.prevent="markAsDone(todo)"> Done </a>
            </div>
        </div>
    </section>
</template>

<script>
import { mapGetters } from 'vuex'

export default {
    name: 'TodoList',
    computed: {
        ...mapGetters([
            'todos'
        ])
    },
    methods: {
        markAsDone(todo) {
            this.$store.dispatch('markAsDone', todo.id)
        }
    }
}
</script>
<style scoped>
.card {
    margin-top: 10px;
  box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 40%;
height: 100px;
  border-radius: 5px;
}

.card:hover {
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
.container{
   margin-top: 5px;
   margin-left: 15px;
}

</style>