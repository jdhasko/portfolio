<template>
    <div class="project-container">
        <div class="flex-box">
        <h2>{{projectName}}.</h2>
        <p class="date">{{date}}</p>
        </div>
        <p>{{description}} </p>
        <p>{{subDescription}}</p>

      
        <div class="picture-gallery"  :class="{'mobile':mobileView}">
            <template v-for="img in imgList" :key="img">
                     <img :src="require(`@/assets/${img.url}`)" :alt="img.alt"/>
            </template>
        </div>

    </div>
</template>

<script>
export default {
    name:'ProjectComponent',
    props:
    {
        projectName:String,
        date:String,
        description:String,
        subDescription:String,
        imgList:[Object],
        mobileView:Boolean
    }
}
</script>

<style scoped>
.project-container
{
    width: 80%;
    margin: 5% auto;
}

.flex-box
{
    display: flex;
    justify-content: space-between;
}

.project-container h2 
{
    font-size: 58px;
    padding: 0;
}
.project-container p
{
    text-align: justify;
}
p.date
{
    margin: 0;
    padding: 2% 0px;
}
.picture-gallery img
{
    margin: 2%;
    width: 90%;
    vertical-align: top;
}
.mobile img
{
    width: 27%;
}
@media screen and (max-width:1200px)
{
    .project-container
{
    width: 80%;
    margin: auto;

}
}
</style>