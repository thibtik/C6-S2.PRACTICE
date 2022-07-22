<template>
    <form  @submit.prevent="addName">
        <div class="friend-form">
           <input v-model="firstName" type="text" placeholder="First Name" class="form-control">
           <input v-model="lastName" type="text" placeholder="Last Name" class="form-control">
           <input v-model="description" type="text" placeholder="Description" class="form-control">
           <div class="skill">
               <input v-model="skill" type="checkbox" id="PHP" name="vehicle1" value="PHP">
               <label for="vehicle1"> PHP</label>
               <input v-model="skill" type="checkbox" id="OOP" name="vehicle2" value="OOP">
               <label for="vehicle2"> OOP</label>
               <input v-model="skill" type="checkbox" id="Vue" name="vehicle3" value="Vue">
               <label for="vehicle3"> VueJS</label>
               <input v-model="skill" type="checkbox" id="Laravel" name="vehicle4" value="Laravel">
               <label for="vehicle4"> Laravel</label>
           </div>
           <button type="submit"  class="btn" >ADD</button>
       </div>
    </form>
    
</template>
<script>
function unquidId(){
    return new Date().getTime();
}
export default{ 
        emits:'add-data',
        data(){
            return{
                firstName:'',
                lastName:'',
                description: '',
                skill:[],
            }
        },
        methods:{
            addName(){
                this.$emit('add-data',unquidId, this.firstName, this.lastName,this.description,this.skill);

            },        
        }
    }
    
</script >
<style scoped>
.friend-form{
    width: 45%;
    height: 310px;
    margin: auto;
    background: rgb(255, 255, 255);
    border-radius: 0.5rem;
    padding: 15px;
    margin-top: 20px;
    border-radius: 10px;
    box-shadow: 1px 1px 5px 3px rgba(192, 189, 189, 0.587);
}
.friend-form input, .btn{
    width: 98%;
    padding: 15px;
    margin: 10px;
    box-sizing: border-box;
    border-radius: 5px;
}
.btn{
    background: rgb(39, 136, 39);
    color: rgb(254, 254, 254);
}
.skill {
    display: flex;
    justify-content: space-evenly;

}
label{
    margin: auto;
    display: flex;
    margin-right: 30px;
}
</style>