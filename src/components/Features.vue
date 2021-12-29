<template>
    <div class="features_value">
   {{reasonvalue}}
    </div>    
     <div class="features_title">
   {{reasontitle}}
    </div>    
     <div class="features_content">
         {{reasoncontent}}
    </div>    
     <div>
    </div>    
</template>

<script>


export default {
 name:"Feature",
 props:["reasonvalue","reasontitle","reasoncontent"]

}
</script>

<style scoped>
.features_value{
color: #17b3e4;
    font-size: 48px;
    font-weight: 300;
    margin-bottom: 10px;
}

.features_title {
color: #17b3e4;
    font-size: 22px;
    font-weight: 600;
    padding: 20px 0;

}

.features_content{
font-family: "Lato", sans-serif;
    line-height: 25px;
    color: #72797a;
    font-size: 18px;
    font-weight: 400;
    padding: 0 30px;
}
</style>
