<template>
<div class="flex-box">
  <MenuBarComponent 
  :menuObjects="[{name:'Home', menuOption:'Home'},{name:'Contact',menuOption:'Contact'}]" 
  />
  <template v-if="menu ==='Home'">
    <div class="home-main">
      <h2>My UI design projects</h2>

      <div class="grid-box">
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent :projectName="'twister.'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>

      </div>
    </div>
  </template>
    <template v-if="menu ==='Contact'">
    <div></div>
  </template>
</div>
</template>

<script>
import MenuBarComponent from "./components/MenuBarComponent.vue";
import ProjectDisplayComponent from "./components/ProjectDisplayComponent.vue"

export default {
  name: "App",
  data(){
    return{
      menu:'Home'
    }
  },
  components: {
    MenuBarComponent,
    ProjectDisplayComponent
  },
};
</script>

<style>
#app {
  font-family: "Times New Roman", Times, serif, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
}
html,body {
  margin: 0;
}
h2,h3
{
  font-weight: normal;
  margin: 0;
}

.flex-box
{
  display: flex;
}
.home-main
{
  margin: auto;
  width: 80vw;
  height: 100vh;
  background: #EEEEEE;
}

.grid-box
{
  margin: 7vh 7%;
  display:grid;
  grid-template-columns: auto auto auto auto ;
  grid-template-rows: auto auto;
  row-gap: 10%;

  column-gap: 3%
}
h2
{
  text-align: left;
  padding: 5% 7% 0%;
  
}

</style>
