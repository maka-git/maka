<template>
  <div>
      <a-row>
          <a-col :span="16" :offset="4" :style="{marginTop:'40px'}">
            <a-row>
              <a-col :span="6" class="populartitle">
                <div>
                  <p>Popular Categories</p>
                  <div class="line">
                      <a-row>
                      <a-col :span="12" class="aa">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>LDPE</a></div>
                      </a-col>
                      <a-col :span="12" class="bb">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>HDPE</a></div>
                      </a-col>
                  </a-row>
                  <a-row>
                      <a-col :span="12" class="aa">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PP</a></div>
                      </a-col>
                      <a-col :span="12" class="bb">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PP/PET</a></div>
                      </a-col>
                  </a-row>
                  <a-row>
                      <a-col :span="12" class="aa">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PET</a></div>
                      </a-col>
                      <a-col :span="12" class="bb">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PS/ABS</a></div>
                      </a-col>
                  </a-row>
                  <a-row>
                      <a-col :span="12" class="aa">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>ABS</a></div>
                      </a-col>
                      <a-col :span="12" class="bb">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PMMA</a></div>
                      </a-col>
                  </a-row>
                  <a-row>
                      <a-col :span="12" class="aa">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>PVC</a></div>
                      </a-col>
                      <a-col :span="12" class="bb">
                          <div><a><a-icon type="container"></a-icon></a></div>
                          <div><a>Other</a></div>
                      </a-col>
                  </a-row>
                  </div>
                </div>
              </a-col>
              <a-col :span="12">
                <a-carousel arrows autoplay>
                    <div
                    slot="prevArrow"
                    class="custom-slick-arrow"
                    style="left: 10px;zIndex: 1"
                    >
                    <a-icon type="left-circle" />
                    </div>
                    <div slot="nextArrow" class="custom-slick-arrow" style="right: 10px">
                    <a-icon type="right-circle" />
                    </div>
                    <div><a href="" class="aaa"><img src="../../assets/images/01.png" alt=""></a></div>
                    <div><a href="" class="aaa"><img src="../../assets/images/02.png" alt=""></a></div>
                    <div><a href="" class="aaa"><img src="../../assets/images/03.png" alt=""></a></div>
                    <div><a href="" class="aaa"><img src="../../assets/images/04.png" alt=""></a></div>
                    <div><a href="" class="aaa"><img src="../../assets/images/05.png" alt=""></a></div>
                </a-carousel>
              </a-col>
              <a-col :span="6" class="populartitle">
                  <div>
                  <p>welcome</p>
                  <div class="line">
                    <form action="">
                        <label for="">
                            <span class="disp-blk">Account</span>
                            <input type="text" placeholder="Please enter your email" class="disp-blk-input1">
                        </label>
                        <label for="" class="eyeposition">
                            <span class="disp-blk">Password</span>
                            <input :type="pwdType" placeholder="Please enter your password" class="disp-blk-input2">
                            <a-icon :type="eyeType" class="eye" @click="showhide()"></a-icon>
                        </label>
                        <label for="">
                            <a-button class="sign" type="primary"><a-icon type="lock"></a-icon> Sign In</a-button>
                        </label>
                        <label for="" class="mima">
                            <a>Register Free</a>
                            <a>Forgot Psaaword?</a>
                        </label>
                        <label for="" class="prn">
                            <a href="">
                                <p><a-icon type="export"></a-icon></p>
                                <p class="prn-p">PRN</p>
                            </a>
                            <a href="">
                                <p><a-icon type="export"></a-icon></p>
                                <p class="prn-p">Price Pattern</p>
                            </a>
                            <a href="">
                                <p><a-icon type="export"></a-icon></p>
                                <p  class="prn-p">Logistics</p>
                            </a>
                        </label>
                    </form>
                  </div>
                </div>
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
        pwdType: 'password',
        eyeType: 'eye-invisible'
    }
  },
  methods: {
      showhide() {
        this.pwdType = this.pwdType === 'password' ? 'text' : 'password';
        this.eyeType = this.eyeType === 'eye-invisible' ? 'eye' : "eye-invisible"
      }
  }
}

</script>

<style  scoped lang="less">
@import "../../assets/css/views/main/welcome.less";

</style>

// 轮播图
<style scoped>
/* For demo */
.ant-carousel >>> .slick-slide {
  text-align: center;
  height: 371.4px;
  line-height: 160px;
  /* background: #364d79; */
  overflow: hidden;
}

.ant-carousel >>> .custom-slick-arrow {
  width: 25px;
  height: 25px;
  font-size: 25px;
  color: #fff;
  background-color: rgba(31, 45, 61, 0.11);
  opacity: 0.3;
}
.ant-carousel >>> .custom-slick-arrow:before {
  display: none;
}
.ant-carousel >>> .custom-slick-arrow:hover {
  opacity: 0.5;
}

.ant-carousel >>> .slick-slide h3 {
  color: #fff;
}
</style>