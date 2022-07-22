<template>
    <Navbar/>
    <Form @add-data='addFriend'></Form>
    <Card v-for="friend of friends" :key="friend" :friend="friend" :methodDelete="deleteData"></Card>
</template>

<script>
import Navbar from './components/NavbarView.vue'
import Form from './components/FormView.vue'
import Card from './components/CardView.vue'
export default {
  name: 'App',
  components: {
    Navbar,
    Form,
    Card,
  },
  data(){
    return{
      friends:[
        // {FirstName:'Thib', LastName:'Tik',descriptions:"The best"},
      ]
    }
  },
  methods:{
    addFriend(unquidId,firstName, lastName, description,skill){
      this.friends.push({id:unquidId(),FirstName:firstName, LastName:lastName, descriptions:description,skills:skill})
    },
    deleteData(id){
      const index = this.friends.findIndex(friend => friend.id === id);
      this.friends.splice(index, 1);
    }
  }

}
</script>

<style>

</style>
