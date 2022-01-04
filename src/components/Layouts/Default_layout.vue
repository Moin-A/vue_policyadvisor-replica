<script>
import Footer from '../Footer.vue'
import Header from '../Header.vue'


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
