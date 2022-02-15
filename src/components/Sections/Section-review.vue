<template>
<div class="row justify-content-center " >
    <div class="col-8 ">
    <div class="d-flex">
    <div class="mr-2">
        <img src="../../assets/reviews-dial.png"/>
    </div>
    <div>
        <img src="../../assets/review-rating.png"/>
    </div>
    <carousel/>
    </div>
    <div><MyComponen/></div>
    </div>
   </div>
</template>

<script>
import MyComponen from "../UI/Slider/Slider.vue";

export default {
  
name:"Section_Review",
components:{
MyComponen
},


 
}



</script>

<style scoped>
 p {
    font-weight: 600;
    font-size: 2rem;
    text-align: left;
 }
 .hero-image{
 background-image: url('~@/assets/Hero-image.png');
 background-size: cover;
 height: 47vw;
 background-size: cover;
 background-position: center;
}
@media screen and (max-width: 760px) {
.hero-image{
 background-image: url('~@/assets/Hero-image-pink-optimised.png')!important;  
 background-size:cover;
 background-repeat: no-repeat;
 height: 40vw ;
}

}
.main-content {
   top:0px;
   bottom:0px;
   left:0px;
   right:0px;
}
@media screen and (max-width: 1070px) {

.main-content_text {
    position:absolute;
    top:0px;
    display:flex;
    justify-content: center;
    width: 80%;
    text-align: center;
    color: #fff;   
}
.main-content_text p {
   text-align: center;
}
}
@media screen and (min-width: 1070px) {
  .main-content {
position: absolute;
  } 
}
</style>
