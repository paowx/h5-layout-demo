<template>
  <div class="index-warp">
    <!--首页广告位-->
    <div class="index-swiper">
      <img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/20190902/43fca762f2fdca6cca9a81ad354326c9.png?x-oss-process=image/watermark,image_ZmFuZ3poaWxpYW9fd2F0ZXIucG5nP3gtb3NzLXByb2Nlc3M9aW1hZ2UvcmVzaXplLHdfNTM5,t_90,g_se,x_26,y_22"/>
    </div>
    <!--icon-->
    <div class="icon-list">
      <div @click="goto(4)" class="icon-item">
        <div class="img-panel"><img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-zxf.png" alt=""></div>
        <p class="icon-text">找新房</p>
      </div>
      <div @click="goto(5)" class="icon-item">
        <div class="img-panel"><img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-mfzx.png" alt=""></div>
        <p class="icon-text">买房咨询</p>
      </div>
      <div @click="goto(6)" class="icon-item">
        <div class="img-panel"><img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-spkf.png" alt=""></div>
        <p class="icon-text">视频看房</p>
      </div>
      <a href="https://m.gdfangpin.com/kanfang#/" class="icon-item">
        <div class="img-panel"><img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-kft.png" alt=""></div>
        <p class="icon-text">看房团</p>
      </a>
      <div @click="goto(8)" class="icon-item">
        <div class="img-panel"><img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-lszx.png" alt=""></div>
        <p class="icon-text">楼市资讯</p>
      </div>
    </div>

    <!--推荐楼盘-->
    <!--<div class="loupan-temp">
      &lt;!&ndash;<v-title tit="推荐楼盘" href="https://lp.gdfangpin.com/houseList/" :hf="true" moreText="查看全部"></v-title>&ndash;&gt;
      <div class="loupan-list">
        <a href="http://baidu.com" class="loupan-item">
          <div class="lp_sell_status">特惠</div>
          <div class="left-panel">
            <img src="https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/20191018/cae47ff3bc53b599b3fe87dba989c0a0.png" alt="">
          </div>
          <div class="right-panel">
            <div class="lp_name">美林湖</div>
            <div class="bright-spot">提啊付过款发动机盖</div>
            <div class="lp_area"><span class="area">广州<span>不发个</span></span><span class="lp_floorage">建面40-90㎡</span></div>
            <div class="tags">
              <span class="tag-item">在售</span>
              <span class="tag-item">住宅</span>
              <span class="tag-item"></span>
            </div>
            <div class="lp_price">32000<span class="see-house">专车看房</span></div>
            <div class="zhekou">
              <span class="zhekou-span">不干活</span>
            </div>
          </div>
        </a>
      </div>
    </div>-->
  </div>
</template>

<script>
  export default {
    data() {
      return {}
    },
    computed: {
    },
    mounted() {
    },
    components: {
    },
    activated() {
    },
    methods: {
      goto(type) {
        switch (type) {
          case 4:
            window.location.href = window.HOST2 + '/houseList'
            break
          case 5:
            this.$router.push({name: 'qa'})
            break
          case 6:
            window.location.href = window.HOST2 + '/houseList?lp_tags=视频看房'
            break
          case 8:
            window.location.href = window.HOST2 + '/informationList'
            break
        }
      }
    }
  }
</script>

<style lang="scss">
  .index-warp{
    margin: auto;
    .header-warp{
      height: 2.5rem;
      background: #ffffff;
      border-bottom: 1px solid #E5E5E5;
      display: flex;
      padding: 0 1rem;
      box-sizing: border-box;
      position: relative;
      .logo-a{
        display: inline-block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        img{
          height: .75rem;
          width: auto;
          display: block;
        }
      }
      .user-search{
        display: inline-block;
        position: absolute;
        top: 50%;
        right: 1rem;
        transform: translateY(-50%);
        img{
          width: .8rem;
          height:.8rem;
          display: block;
        }
        .search-a{
          display: inline-block;
          padding: 0 .4rem;
        }
        .user-a{
          display: inline-block;
        }
      }
    }
    .index-swiper{
      height: 290px;
      padding: 40px;
      background: #ffffff;
      overflow: hidden;
      img{
        width: 100%;
        height: 100%;
      }
    }
    .second-swiper{
      height: 4.5rem;
      padding: .75rem 1rem .75rem 1rem;
      background: #ffffff;
      margin-bottom: .4rem;
      .mint-swipe{
        border-radius: 4px;
        overflow: hidden;
        img{
          width: 100%;
          height: 100%;
          border-radius: 4px;
        }
      }
    }
    .icon-list{
      display: flex;
      padding: 40px;
      background: #ffffff;
    }
    .icon-item{
      flex: 1;
      margin: auto;
      text-align: center;
      color: #656565;
      .img-panel{
        margin: auto;
        text-align: center;
      }
      img{
        width:82px;
        height:82px;
        display: block;
        margin: auto;
      }
      .icon-text{
        font-size: 24px;
      }
    }
    .zx-panel{
      padding: 0 1rem 0 1rem;
      box-sizing: border-box;
      background: #ffffff;
      .border-div{
        border-top: 1px solid #E5E5E5;
        display: flex;
        box-sizing: border-box;
        padding: .4rem 0rem .7rem 0rem;
      }
      .zx-tit{
        font-size: .9rem;
        font-weight: bold;
        padding-right: 1rem;
        line-height: 1.5rem;
        vertical-align: middle;

        img {
          width: 58px;
          height: 13px;
        }
      }
      .zx-content{
        flex: 1;
        text-overflow: ellipsis;
        white-space: nowrap;
        min-width: 0;
        font-size: .7rem;
        line-height: 1.5rem;
        vertical-align: middle;
        color: #2C2C2C;
        .swiper-container{
          height: 1.5rem;
        }
      }
    }
    .tit-div{
      display: flex;
      padding: .8rem;
      position: relative;
      .tit{
        position: relative;
        flex: 1;
        font-size: .9rem;
        font-weight: bold;
        line-height: 1.5rem;
      }
      .more{
        /*width: 50px;*/
        /*text-align: right;*/
        position: relative;
        font-size: .6rem;
        color: #999999;
        vertical-align: middle;
        padding-right: 15px;
        line-height: 1.5rem;
      }
      .arrow{
        border-top: 1px solid #999999;
        border-right: 1px solid #999999;
        border-left-width: 0;
        border-bottom-width: 0;
        width: 8px;
        height: 8px;
        display: inline-block;
        position: absolute;
        top: 50%;
        right: 0;
        transform: translate(-50%, -50%) rotate(45deg);
      }
    }
    .loupan-list{
      padding: 0 1rem;
      background: #ffffff;
      .loupan-item{
        display: flex;
        padding: 1rem 0;
        border-bottom: 1px solid #E5E5E5;
        position: relative;
        .lp_sell_status{
          position: absolute;
          top: 1rem;
          right: 0;
          background:linear-gradient(-16deg,rgba(255,153,51,1),rgba(255,119,9,1));
          border-radius:10px 10px 10px 0px;
          color: #ffffff;
          font-size: .5rem;
          font-weight: 200;
          /*width: 2.1rem;*/
          line-height: 1;
          padding: .15rem .35rem;
          text-align: center;
        }
        .left-panel{
          img{
            width: 5.25rem;
            height: 4rem;
            border-radius: 2px;
          }
          padding-right: 1rem;
        }
        .right-panel{
          flex: 1;
          line-height: 1;
          min-width: 0;
          .lp_name{
            color: #313131;
            font-size: .8rem;
            font-weight: bolder;
            margin-bottom: .4rem;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            width: 80%;
            line-height: 1.1;
          }
          .bright-spot{
            font-size: .5rem;
            color: #353535;
            padding-bottom: .3rem;
          }
          .lp_area{
            color: #9f9f9f;
            font-size: .55rem;
            white-space: nowrap;
            text-overflow: ellipsis;
            .lp_floorage{
              display: inline-block;
              padding-left: .5rem;
              border-left: 1px solid #b2b2b2;
            }
            .area{
              display: inline-block;
              padding-right: .5rem;
            }
          }
          .tags{
            padding-top: .3rem;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            font-size: 0;
          }
          .tag-item{
            display: inline-block;
            color: #8EAAE3;
            background: #F1F7FD;
            font-size: .5rem;
            padding: 0 .2rem;
            border-radius:2px;
            margin-right: .25rem;
            line-height: .8rem;
          }
          .lp_price{
            color: #EE1F1F;
            font-weight: bolder;
            font-size: .7rem;
            padding-top: .3rem;
            vertical-align: middle;
            .see-house{
              display: inline-block;
              vertical-align: middle;
              background: #FFEBEB;
              color: #F66B07;
              font-size: .5rem;
              padding: 0 .2rem;
              line-height: .9rem;
              border-radius:2px;
              font-weight: normal;
              margin-left: .25rem;
            }
          }
        }
        .zhekou{
          margin-top: .2rem;
          .zhekou-span{
            color: #FF7B00;
            display: inline-block;
            background: url("https://fcpdlpk.oss-cn-shenzhen.aliyuncs.com/apps/wap/wap-discount.png") center no-repeat;
            background-size: 100% 100%;
            /*height: .9rem;*/
            line-height: .9rem;
            padding: 0 .3rem;
            font-size: .5rem;
          }
        }
      }
      .loupan-item:last-child{
        border-bottom: none!important;
      }
    }
  }

</style>
