<template>
  <div class="home">
    <BennerCotenido/>
      <Main/>
      <Main2/>
      <Main3/>
      <Footer/>
  </div>
</template>

<script>
import Footer from '../components/Footer'
import Main3 from '../components/Main3'
import Main2 from '../components/Main2'
import Main from   '../components/Main'
import BennerCotenido from '../components/BennerCotenido'
export default {
  name: 'Home',
  components:{
   BennerCotenido, Main,
   Main2,Main3,Footer,
 }
  
}
</script>
