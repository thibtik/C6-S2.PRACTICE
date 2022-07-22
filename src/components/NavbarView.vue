<template>
    <div class="friend-nav">
      <ul  >
       <li><a :href="HomeLink">HOME</a></li>
        <li><a :href="aboutLink">About</a></li>
        <li><a :href="flower">flower</a></li>
        <li><a href="#">Login</a></li>
        <li><a href="#">Register</a></li>
      </ul>
  </div>
</template>

<script>
export default {
    data(){
        return{
            HomeLink:'https://vuejs.org/',
            aboutLink:'https://mooreviewsdotcom.files.wordpress.com/2022/03/pixar-turning-red-panda.jpeg',
            flower:'https://cdn.britannica.com/84/73184-004-E5A450B5/Sunflower-field-Fargo-North-Dakota.jpg'
        }
    }
 };
</script>

<style scoped>
* {
    box-sizing: border-box;
  }
  html {
    font-family: 'Jost', sans-serif;
  }
  #app ul {
    margin: 0;
    padding: 0;
    list-style: none;
    background:rgb(228, 119, 137);
    display: flex;
  }
  
#app li {
    margin: 15px;
}
a{
  color: antiquewhite;
  text-decoration: none;
}

</style>