<template>
  <div>
    <tab-bar></tab-bar>
    <welcome/>
    <material/>
    <solution/>
    <deals/>
    <logistics/>
    <news/>
    <Footer/>
  </div>
</template>

<script>
import TabBar from './header/TabBar'
import Welcome from '../views/main/welcome'
import Material from '../views/material'
import Solution from '../views/solution'
import Deals from '../views/deals'
import Logistics from '../views/logistics'
import News from '../views/news'
import Footer from './footer/footer'
export default {
  data () {
    return {
    }
  },
  components:{
    TabBar,
    Welcome,
    Material,
    Solution,
    Deals,
    Logistics,
    News,
    Footer
  }
}
</script>

<style  scoped>

</style>
