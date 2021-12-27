<template>
<div class="position-relative">
   <div class="hero-image"  >      
   </div> 
 
      <div class="row main-content justify-content-around mx-sm-5 pt-5 mx-2">   
     <div class="col-lg-4 main-content_text"><p>The easiest way to get a life insurance policy online</p></div>
     <div class="col-lg-6 col-md-8 col-sm-8 col-xl-5 col">
       <Widget/>
     </div>
   </div>  
   </div>
</template>

<script>
 import Widget from "./Widget-form.vue";

export default {
name:"TopSection",
components:{
  Widget 
}
 
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
