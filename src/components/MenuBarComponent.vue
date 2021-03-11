<template>
    <div id="menu-container">
        <div class="flex-container">
            <div id="logo-container">
                <h2>Dominik János<br>Haskó</h2>
            </div>
            <div id="menu-options-container">
                <ul>
                    <template v-for="option in menuObjects" :key="option">
                     <li v-on:click="menuChange(option.menuOption)" ><a class="left">{{option.name}}</a></li>
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
    methods:
    {
        menuChange(menuOption) 
        {
            this.$emit('menuChange', menuOption);
            console.log("asd")
        }
    }


}
</script>

<style scoped>
#menu-container
{
    position: fixed;
    height: 100%;
    width: 19vw;
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
@media screen and (max-width:1200px){
    #menu-container{
        height: auto;
        z-index: 1;
        width: 100%;
    }
    #logo-container
    {
       margin: auto 0px;
        width:fit-content;
        white-space: nowrap;
    }
    #logo-container h2{
    font-size: 15px;

    }
    #menu-options-container
    {
        padding: 3%;
    }

    #menu-options-container ul
    {
        padding:0;
        margin: 0;
        vertical-align: bottom;
    }
    #menu-options-container li{
    display: inline;
    list-style: none;
    font-size: 16px;
    padding: 5px 15px;
    margin: 0% 0%;
    width: auto;
    }
    #menu-options-container li a
    {
    display: inline;

    }

    .flex-container 
    {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }

    #title-container
    {
    display: block;
    padding: 1%;
     margin: auto 0px;
    }

    #title-container h1{
     display: block;
    font-weight: normal;
    font-size: 25px;
    text-decoration: underline;
    writing-mode:horizontal-tb;
    transform: rotate(0deg);
    margin: 0;
    padding: 0%;
    }

    a.left:hover:before {
    visibility: visible;
    width: 100%;
}
  
}

</style>