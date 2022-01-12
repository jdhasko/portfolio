<template>
<div class="flex-box">
  <MenuBarComponent @menuChange="(menuChange($event))"
  :menuObjects="[{name:'Home', menuOption:'Home'},{name:'Contact',menuOption:'Contact'}]" 
  />
  <template v-if="menu ==='Home'">
    <div class="home-main">
      <h2>My UI design projects</h2>

      <div class="grid-box">
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="twister" :projectName="'Twister'" imgUrl="projects/twister/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="jdhasko" :projectName="'jdhasko.github.io'" imgUrl="projects/jdhasko/logo.png" :imgAlt="'Jdhasko logo.'"/>
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="fevr" :projectName="'FevR'" imgUrl="projects/fevr/logo.png" :imgAlt="'Twister logo.'"/>
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="mindeladlak" :projectName="'mindeladlak'" imgUrl="projects/mindeladlak/logo.png" :imgAlt="'Mindeladlak logo.'"/>
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="parkandgarden" :projectName="'Park and Gaden.'" imgUrl="projects/parkandgarden/logo.png" :imgAlt="'Park and Garden logo.'"/>
      <ProjectDisplayComponent @menuChanged="(menuChange($event))" menuName="orchid" :projectName="'Orchid'" imgUrl="projects/orchid/logo.png" :imgAlt="'Orchid logo.'"/>

      </div>
      <p>Please note that the page is just a demo and under construction</p>
    </div>
  </template>
    <template v-if="menu ==='Contact'">
        <div class="side-align">
</div>
  </template>

  <template v-if="menu ==='twister'">
        <div class="side-align">

      <ProjectComponent :projectName="'twister'" date="February 2021"  description='Twister was designed as part of my mandatory assignment in mobile app development. Twister is a "twitter-like" app.
        The main goal of the application to serve as a new and positive social application. While working on the UI design my main 
        goal was to remove those elements which can cause harm in the user. (Such as number of followers, likes etc.)
        The application aims to help people spreading positivity and connecting with each other. 
        The design was created in Adobe Xd, and the project is still on-going so updates or changes may appear.
        ' 
        :mobileView='true'
        :imgList="[
        {url:'projects/twister/Twister-LoginPage.png', alt:'Login Screen'},
        {url:'projects/twister/Twister-RegisterPage.png', alt:'Register Screen'},
        {url:'projects/twister/Twister-ProfilePage.png', alt:'Login Screen'},
        {url:'projects/twister/Twister-HPage.png', alt:'Profile Screen'},
        {url:'projects/twister/Twister-ProfileEditPage.png', alt:'Login Screen'},
        {url:'projects/twister/Twister-TrendingPage.png', alt:'Trending Screen'},
        ]" 
         />
         </div>
  </template>


  <template v-if="menu ==='jdhasko'">
    <div class="side-align">
        <ProjectComponent :projectName="'jdhasko'" date="January 2021"  
        description=
        '
        The goal with this project was to create my personal website that not only represents me in the content but in the design too.
        I wanted to create something different, something brave, something that has a piece of my heart. The first version of the website 
        and the design were created in 2020. In 2021 I reimagined this single-page site and created a clearer, more user friendly design.
        I relaised my mistakes from the first design, and took them into count while creating the new one thus increasing the readability of the site.
        In the second version, the website also got a proper mobile-view design.
        ' 
        :mobileView='false'
        :imgList="[
        {url:'projects/jdhasko/aboutMe.png', alt:'Login Screen'},
                {url:'projects/jdhasko/logo.png', alt:'Login Screen'},

        {url:'projects/jdhasko/values.png', alt:'Login Screen'},
        ]" />
    </div>
  </template>
    
  <template v-if="menu ==='fevr'">
    <div class="side-align">
        <ProjectComponent :projectName="'fevr'" date="November 2020"  
        description=
        '
         FevR was created as part of my studies at Zealand. Fevr was our soulution for our
         3rd semester exam in Programming and Software Design. Fevr is a high-temperature detecting system that was to be implemented by
         local authorities and private companies. The purpose of FevR is to prevent the spread of COVID-19 and other diseases on public
         places. The device could be installed in the entrance of public places. It gives immediate feedback if one has fever or not
         and keeps a record of the test-data. Some part of this data is publicly accessible for everyone and some part of it is
         protected and only can be seen by the responsible user.
        ' 
        subDescription='
         Our solution is a collection of softwares and physical devices. It includes a sensor which is a Raspberry PI equipped with
         an infrared thermometer sensor which broadcasts data on the local network to a server which sends the data to the API that
         records the data in the database. The API and the database are located in the Azure Cloud.
         The data is accessible on the FevR web-application. Here you can see the design of the web-app.


         The project has been carried out and we passed both subjects with 12.
         The frontend was coded using React.
         '
        :mobileView='false'
        :imgList="[
        {url:'projects/fevr/Login-page.png', alt:'Login Screen'},
        {url:'projects/fevr/Home.png', alt:'Home screen'},
        {url:'projects/fevr/Map-view.png', alt:'Map-view screen'},
        {url:'projects/fevr/DevicesPage.png', alt:'Map-view screen'},
        {url:'projects/fevr/ListView.png', alt:'List-view screen'},
        {url:'projects/fevr/ProfilePage.png', alt:'Map-view screen'},


        ]" />
    </div>
  </template>
  <template v-if="menu ==='mindeladlak'">
    <div class="side-align">
        <ProjectComponent :projectName="'mindeladlak'" date="September 2020"  
        description=
        '
        This design was created for www.mindeladlak.hu. The solution has not been implemented yet but the project might start during the summer.
        The goal was to create a more modern, user friendly web-page instead of the existing old-fashioned one.
        ' 
        subDescription="Mindeladlak is a real-estate agency based in Hungary. I approached them with the idea of a new design and they were open
        for co-operation."
        :mobileView='false'
        :imgList="[
        {url:'projects/mindeladlak/logo.png', alt:'logo'},
        {url:'projects/mindeladlak/HomePage.png', alt:'logo'},
        {url:'projects/mindeladlak/SearchPage.png', alt:'logo'},
        ]" />
    </div>
  </template>

  <template v-if="menu ==='parkandgarden'">
    <div class="side-align">
        <ProjectComponent :projectName="'Park and Garden'" date="December 2021"  
        description=
        '
          This project has started as part of my final exam project (dissertation) in Computer Science at Zealand Academy in Roskilde.
          It is part of a digitalization solution that has been delivered to a Hungarian business that works in floristry and gardening. 
          The company previously did not have any online availabilities, nor a cohesive brand design. For this reason the following website, webshop, logo and other visuals were delivered. 
        ' 
        subDescription="A demo of the website can be seen at: www.parkeskert.com"
        :mobileView='false'
        :imgList="[
        {url:'projects/parkandgarden/logo.png', alt:'logo'},
        {url:'projects/parkandgarden/homepage.png', alt:'Home page'},
        ]" />
    </div>
  </template>
    <template v-if="menu ==='orchid'">
    <div class="side-align">
        <ProjectComponent :projectName="'Orchid'" date="December 2021"  
        description=
        '
        Orchid is an an Inventory management and Cash registry mobile application designed for tablets. This design was created as my final exam in Computer Science at Zealand Academy in Roskilde.
        
        ' 
        subDescription="A demo of the website can be seen at: www.parkeskert.com"
        :mobileView='false'
        :imgList="[
        {url:'projects/orchid/homescreen.png', alt:'Home page'},
        {url:'projects/orchid/productscreen.png', alt:'Home page'},
        {url:'projects/orchid/cashscreen.png', alt:'Home page'},
        {url:'projects/orchid/loginscreen.png', alt:'Home page'},
        ]" />
    </div>
  </template>
</div>
</template>

<script>
import MenuBarComponent from "./components/MenuBarComponent.vue";
import ProjectDisplayComponent from "./components/ProjectDisplayComponent.vue"
import ProjectComponent from "./components/ProjectComponent"

export default {
  name: "App",
  data(){
    return{
      menu: "Home"
    }
  },
  components: {
    MenuBarComponent,
    ProjectDisplayComponent,
    ProjectComponent
  },
  methods: {
    menuChange(newMenu)
    {
      this.menu = newMenu;
      console.log("menu changed :" + newMenu  )
    }
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
  background: #EEEEEE ;
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
  width: 80vw;
  height: auto;
  background: #EEEEEE;
  margin-left: 19vw;
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
.side-align
{
  margin-left: 19vw;
}

@media only screen and (max-width: 1200px) {
  .flex-box
  {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  .home-main
  {
    margin: 12% auto ;
  }
  .grid-box
  {
  grid-template-columns: auto ;
  grid-template-rows: auto auto auto auto ;
  row-gap: 3%;
  }
  .side-align
  {
    margin: auto;
    margin-top:12%;
  }
}

</style>
