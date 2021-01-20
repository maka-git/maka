<template>
  <div>
    <a-row>
        <a-col :span="16" :offset="4">
        <a-row class="header-bar">
            <a-col :span="12">hello,welcom to 99Plas! <span><a href="">Sign In</a></span><a href="" class="free">Register Free</a></a-col>
            <a-col :span="12" class="col-left">
                <span><a href="">Are you a buyer?</a></span>
                <span class="free" :style="{paddingRight:'0'}">
                <a href=""><img src="../../assets/images/flags.png" alt="" width="50px"></a>
                <span ><a href="">English - GBP</a></span>
                <a-icon type="down"></a-icon>
                </span>
            </a-col>
        </a-row> 
    </a-col> 
    </a-row>
<!-- logo -->
    <a-row>
        <a-col :span="16" :offset="4">
        <a-row>
            <a-col :span="12">
            <a href=""><img src="//assets-cdn.99plas.com/themes/spring-logo.png" alt=""></a>
            <a href="" class="logo-right tilt"><span style="color:white">Raw Mfaterial Site</span></a>
            <a href="" class="logo-right" style="color: cadetblue">Pellets Sites(Beta)</a>
            </a-col>
            <a-col :span="12" class="col-left" :style="{marginTop:'1em'}">
            <a href="" :style="{marginRight: '1em'}"><a-icon type="user" :style="{fontSize: '2em',color:'grey'}"/>My Account</a>
            <a href=""><a-icon type="message" :style="{fontSize: '2em',color:'grey'}"/>Messages</a>
            </a-col>
        </a-row>
        </a-col>
    </a-row>
<!-- 导航条 -->
    <a-row class="bar">
    <a-col :span="16" :offset="4">
        <a-dropdown>
        <a class="ant-dropdown-link bb solution">
            <a-icon type="menu"></a-icon>
            Categories&nbsp;
            <a-icon type="down" />
            </a>
            <a-menu slot="overlay">
            <a-menu-item>
                <ul class="cate">
                    <li v-for="item in Categories" :key="item.message">{{item.message}}</li>
                </ul>
            </a-menu-item>
            <!-- <a-menu-item>
                <ul class="cate">
                    <li >HDPE</li>
                    <li >PE/PET</li>
                    <li>PET</li>
                    <li>PP/PE</li>
                </ul>
            </a-menu-item>
            <a-menu-item>
                <ul class="cate">
                    <li >PP</li>
                    <li >BOPP</li>
                    <li>PS</li>
                    <li>EPS</li>
                </ul>
            </a-menu-item>
            <a-menu-item>
                <ul class="cate">
                    <li>ABS</li>
                    <li>HIPS</li>
                    <li>PC/ABS</li>
                    <li>PS</li>
                </ul>
            </a-menu-item>
            <a-menu-item>
                <ul class="cate">
                    <li>PMMA</li>
                    <li>PVC</li>
                    <li>PA</li>
                    <li>PBT</li>
                </ul>
            </a-menu-item>
            <a-menu-item>
                <ul class="cate">
                    <li>PU/TPU</li>
                    <li>PU</li>
                    <li>TPU</li>
                    <li>Complex</li>
                </ul>
            </a-menu-item> -->
            </a-menu>
        </a-dropdown>
    <a class="solution">Home</a>
    <a class="solution">Demand</a>
    <a class="solution">Blog</a>
    <a-dropdown class="solution aa">
        <a class="ant-dropdown-link">Solution&nbsp;<a-icon type="down"/></a>
            <a-menu slot="overlay">
            <a-menu-item class="solution" >
                <a href="javascript:;" :style="{textAlign:'center'}">Education</a>
            </a-menu-item>
            <a-menu-item class="solution">
                <a href="javascript:;" :style="{textAlign:'center'}">Service</a>
            </a-menu-item>
            </a-menu>
        </a-dropdown>     
    </a-col>
    </a-row>
<!-- 搜索 -->
    <a-row>
      <a-col :span="16" :offset="4">
        <a-row>
            <a-col :span="17" :style="{marginTop: '2em'}">
                <div class="listing">
                    <a-row>
                        <a-col :span="3"> 
                            <a-dropdown :trigger="['click']">
                                <span class="listingspan">
                                    <a class="ant-dropdown-link " @click="typechange">listing <a-icon :type="type" :style="{fontSize:'10px'}"></a-icon></a>
                                </span>
                                <a-menu slot="overlay">
                                <a-menu-item>
                                    <a href="javascript:;" :style="{textAlign: 'center'}">listing</a>
                                </a-menu-item>
                                <a-menu-item>
                                    <a href="javascript:;" :style="{textAlign: 'center'}">Suppliers</a>
                                </a-menu-item>
                                </a-menu>
                            </a-dropdown>
                        </a-col>
                        <a-col :span="16">
                    <a-input :style="{width:'750px',height:'44.5px',border:'none',backgroundColor: 'transparent',paddingRight: '150px'}" placeholder="What are you looking for..."></a-input>
                        </a-col>
                        <a-col :span="5">
                    <a href="">
                    <span class="listingsearch"><a-icon type="search" :style="{fontSize:'20px',marginRight:'5px'}"></a-icon>Search All</span>
                    </a>
                        </a-col>
                    </a-row>
                   
                </div>
            </a-col>
            <a-col :span="7" class="col-right" :style="{marginTop: '2em'}">
                <a class="list">
                    <p>ALll Listing</p>
                </a>
            </a-col>
        </a-row>
      </a-col>
    </a-row>
<!-- 回到顶部 -->
    <tool-bar/>
  </div>
</template>

<script>
import ToolBar from './ToolBar.vue'
export default {
  components: { ToolBar },
  data () {
    return {
        type:'down',
        // Categories1:[
        //     {
        //         message1:"Categories",
        //         message1:"Categories",

        //     }
        // ],
        Categories:[
            {message: 'LLDPE/LDPE'},
            {message: 'LDPE'},
            {message: 'LLDPE'},
            {message: 'MDPE'}
        ]
    }
  },
  commponents:{
    ToolBar
  },
  methods:{
      typechange() {
          this.type = this.type === 'down' ? 'up' : 'down';
      }
  }
}
</script>

<style>
@import "../../assets/css/components/TabBar.css";

</style>
