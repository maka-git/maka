<template>
  <div>
    <div class="toolbar">
      <div class="toolbar-item up" @click="backTop" v-show="isShowing === true" @mouseover="mouseOver1" @mouseleave="mouseLeave1">
        <a-icon type="up"></a-icon>
        <span v-show="top === true">Scroll to Top</span>
        </div>
      <div class="toolbar-item up"  @mouseover="mouseOver2" @mouseleave="mouseLeave2">
        <a-icon type="clock-circle" />
        <a href="">
          <span v-show="Browsing === true">Browsing History</span>
        </a>
      </div>
      <div class="toolbar-item up"  @mouseover="mouseOver3" @mouseleave="mouseLeave3">
        <a-icon type="customer-service" />
        <a href="">
          <span v-show="Contact === true">Contact Us</span>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isShowing:false,
      top: false,
      Browsing: false,
      Contact: false
    }
  },
  mounted () {
    window.addEventListener('scroll', this.scrollToTop)
  },
  destroyed () {
    window.removeEventListener('scroll', this.scrollToTop)
  },
  methods: {
    backTop() {
      const that = this
      let timer = setInterval(() => {
        let ispeed = Math.floor(-that.scrollTop / 18)
        document.documentElement.scrollTop = document.body.scrollTop = that.scrollTop + ispeed
        if (that.scrollTop === 0) {
          clearInterval(timer)
        }
      }, 16)
    },
  scrollToTop () {
    const that = this
    let scrollTop = window.pageYOffset || document.documentElement.scrollTop || document.body.scrollTop
    that.scrollTop = scrollTop
    if (that.scrollTop > 450) {
      that.isShowing = true
    } else {
      that.isShowing = false
    }
  },
  mouseOver1() {
    this.top = true
  },
  mouseOver2() {
    this.Browsing = true
  },
  mouseOver3() {
    this.Contact = true
  },
  mouseLeave1() {
    this.top = false 
  },
   mouseLeave2() {
    this.Browsing = false  
  },
   mouseLeave3() {
    this.Contact = false
  },
}
}
</script>

<style  scoped lang="less">
@import "../../assets/css/components/ToolBar.less";

</style>
