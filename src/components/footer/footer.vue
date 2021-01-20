<template>
  <div>
    <a-row class="footer">
        <a-col :span="16" :offset="4">
            <a-row>
                <a-col :span="8">
                    <a-row class="tutorial">
                        <a-col :span="12">
                            <h2>Tutorial</h2>
                            <a href="">Users' Guide</a>
                        </a-col>
                        <a-col :span="12">
                            <h2>How to Purchase</h2>
                            <a href="">Find Suppilers</a>
                            <a href="">My Offers</a>
                            <a href="">Order Status</a>
                            <a href="">Payment Types</a>
                            <a href="">Ways to receive your order</a>
                            <a href="">Post Demand</a>
                        </a-col>
                    </a-row>
                </a-col>
                <a-col :span="8">
                    <a-row class="email">
                        <a-col :span="16" :offset="4">
                            <a-row>
                                <a-col :span="5">
                                    <a-icon type="customer-service" :style="{fontSize:'50px',color:'green'}"></a-icon>
                                </a-col>
                                <a-col :span="19">
                                    <p>+86 22-25295328</p>
                                    <p>(Mon-Fri 9:00 - 17:30)</p>
                                </a-col>
                                <div class="email-text">
                                    Emai：
                                    <a href="">service@99plas.com</a>
                                </div>
                            </a-row>
                        </a-col>
                    </a-row>
                </a-col>
                <a-col :span="8">
                    <a-row>
                        <a-col :span="8" :offset="8">
                            <div class="erweima">
                                <img src="//assets-cdn.99plas.com/images/qrcode-99p.png" alt="">
                                <p>Scan by Wechat</p>
                            </div>
                        </a-col>
                    </a-row>
                </a-col>
            </a-row>
        </a-col>
        <a-row>
            <a-col :span="24">
                <div class="about">
                    <a href="">About Us</a>
                    <a href="">Help Centre</a>
                    <a href="">Contact Us</a>
                    <a href="">Join Us</a>
                    <a href="">Partners</a>
                    <a href="">Legal Declaration</a>
                    <a href="">Privacy Terms</a>
                    <a href="">Intellectual Property</a>
                    <a href="">Feedback</a>
                    <a href="">Terms of Use</a>
                </div>
                <p>©️ 2018 - 2019 99plas.com. All rights reserved.</p>
            </a-col>
        </a-row>
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
@import "../../assets/css/components/footer.less";

</style>
