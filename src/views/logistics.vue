<template>
  <div>
     <a-row>
      <a-col :span="16" :offset="4" :style="{marginTop:'30px',backgroundColor:'white'}">
        <a-row>
          <a-col :span="8" class="logistics">
              <div class="img">
                  <div class="wenzi">
                    <p><a href="">Global Logistics</a></p>
                    <p><a href="">99Plas provide international trade logistics network. From cargo loading to delivery, Click here for professional one-stop logistic solutions, with global reach.</a></p>
                  </div>
              </div>
              <div class="mask"></div>
          </a-col>
          <a-col :span="8" class="logistics" :style="{padding:'0 5px'}">
              <div class="img img02">
                  <div class="wenzi">
                    <p><a href="">Inspection</a></p>
                    <p><a href="">99Plas holds experienced recyclable materials quality inspection team. Click here for on-site supervision services to closely control product quality, reduce trade risks and protect business interests.</a></p>
                  </div>
              </div>
              <div class="mask"></div>
          </a-col>
          <a-col :span="8" class="logistics" :style="{padding:'0 0 5px 5px'}">
              <div class="img img03">
                  <div class="wenzi">
                    <p><a href="">Finance</a></p>
                    <p><a href="">99Plas provide supply chain financing solutions to resolve business funding difficulties. Click here for high-quality financial resources to tailor efficient, convenient, affordable and considerate commercial assistance.</a></p>
                  </div>
              </div>
              <div class="mask"></div>
          </a-col>
        </a-row>
      </a-col>
    </a-row>
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  }
}
</script>


<style  scoped lang="less">
@import "../assets/css/views/logistics.less";
</style>