<template>
    <div class="friend-card" >
        <h3>{{friend.FirstName}} {{friend.LastName}}</h3>
        <h4>{{friend.descriptions}}</h4>
        <h4>Skills</h4>
        <Skill :skills='friend.skills'></Skill> 
        <Button  @click="methodDelete(friend.id)"></Button>
     </div>
</template>
<script>

import Skill from "./SkillView.vue" ;
import Button from "./ButtonView.vue" ;

export default {
    components:{
        Skill,
        Button,
    },
    props: {
        friend: Object,
        methodDelete: Function,
    },
};

</script>

<style scoped>

.friend-card {
    margin: 20px auto;
    width: 42%;
    border-top: purple 4px solid;
    padding: 10px;
    border-radius: 10px;
    box-shadow: 1px 1px 5px 3px rgba(192, 189, 189, 0.587);
}

</style>