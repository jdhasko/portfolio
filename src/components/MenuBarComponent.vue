<template>
    <div id="menu-container">
        <div class="flex-container">
            <div id="logo-container">
                <h2>Dominik János<br>Haskó</h2>
            </div>
            <div id="menu-options-container">
                <ul>
                    <template v-for="option in menuObjects" :key="option">
                    <div class="link-background">
                     <li v-on:click="menuChange(option.menuOption)" ><a class="left">{{option.name}}</a></li>
                    </div>
                    </template>
                </ul>
            </div>
            <div id="title-container">
                <h1>portfolio.</h1>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name:'MenuBarComponent',
    props:
    {
        menuObjects:[Object]
    },
    


}
</script>

<style scoped>
#menu-container
{
    height: 100vh;
    width: 20vw;
    text-align: left;
    background: white;
}

#logo-container h2
{
    margin: 0;
    font-weight: normal;
    font-size: 18px;
    padding: 5% 8%;
}
#title-container
{
    display: flex;
    justify-content: flex-end;
 
}
#title-container h1{
    font-weight: normal;
    font-size: 150px;
    text-decoration: underline;
    writing-mode:vertical-rl;
    transform: rotate(180deg);
    margin:0;
    margin-right: 3px;
    }

#menu-options-container ul{
    padding: none;
}
#menu-options-container li{
    list-style: none;
    font-size: 24px;
    padding: 2% 2%;
}
a{
    text-decoration: none;   
    color: black; 
}
a.left
{
    position: relative;
}

a.left:before {
  content: "";
  position: absolute;
  width: 0;
  height: 2px;
  bottom: 0;
  left: 0;
  background-color: black;
  visibility: hidden;
  transition: all 0.3s ease-in-out;
}

a.left:hover:before {
  visibility: visible;
  width: 175%;
}


</style>