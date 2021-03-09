<template>
<div class="project-item-container">
  <div class="flex-vertical">
      <img :src="require(`@/assets/${imgUrl}`)" :alt="{imgAlt}"/>
      <h3>{{projectName}}</h3>
  </div>
</div>
    
</template>
<script>
export default {
    name:'ProjectDisplayComponent',
    props:
    {
        imgUrl:String,
        imgAlt:String,
        projectName:String
    }
}
</script>
<style scoped>
.project-item-container
{
    background: white;
    width: 200px;
    height: 220px;
    box-shadow: 2px 2px 5px black;     
    filter: grayscale(100%);
    transition: 0.4s ease-in-out;

}
.project-item-container:hover
{
        filter: grayscale(0%);

 transform: scale(1.1);   
}
.project-item-container  img
{
    width:90%;
    height: 90%;

    padding: 3%;
    margin: auto;

}



.flex-vertical
{
  display: flex;
  flex-direction: column;
}
.home-main h3
{
    text-align: left;
    padding-left: 6%;
}

</style>