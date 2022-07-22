<template>  
    <ul v-for="skill of skills" :key="skill">
        <li>{{skill}}</li>
    </ul> 
</template>
<script>
export default {
     props: {
        skills: Array,
    },
};

</script>