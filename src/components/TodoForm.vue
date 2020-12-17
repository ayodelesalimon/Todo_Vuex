<template>
      <div class="box">
    <form @submit.prevent="add">
        
                <div class="cardd">
            
                <div class="form__box"> <input type="text"
                    class="input"
                    v-model="text"
                    placeholder="Add todo..."
                    required />
                    </div>
                
           
            
                <button type="submit" class="button is-primary"> Add </button>
            
      </div>
       
   </form>
      </div>
</template>

<script>
export default {
    name: 'TodoForm',
    data() {
        return {
            text: ''
        }
    },
    methods: {
        add() {
            this.$store.dispatch('addTodo', this.text)
            this.text = ''
        }
    }
}
</script>
<style scoped>
button{
    margin: 0 auto;
   border-radius: 5px;
    margin-top: 20px;
    width: 150px;
    background-color: rgb(100, 224, 100);
    height: 30px;
    color: beige;
    box-shadow: 0 4px 8px 0 rgba(238, 231, 231, 0.2);
}
button:hover{
    color: green;
    background-color: white;
     box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
}
input{
    border: 1px solid grey;
    border-color: black;
    height: 30px;
    width: auto;
    font-size: 15px;
    font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.box{
 box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
  transition: 0.3s;
  width: 30%;
height: 200px;
  border-radius: 5px;
  justify-content: center;
  padding: 10px;
    
}
.form__box{
margin: 0 auto;
}
.cardd{
    margin-top: 50px;
display: flex;
flex-direction: column;
justify-content: center;
}
</style>
