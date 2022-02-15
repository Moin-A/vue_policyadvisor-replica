<script>
import Footer from '../Marginals/Footer.vue'
import Header from '../Marginals/Header.vue'


export default {
   name:"LayoutDefault",
   components:{
             Header,
             Footer
             }
}
</script>

<template>
<div>
    <Header/>
    
    <slot/>
    <Footer/>
        
</div>        
</template>
