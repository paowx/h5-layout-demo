<template>
  <!--<router-link class="tit-warp" :to="href" v-if="href && !hf">
    <div class="tit-name">{{tit}}</div>
    <div class="tit-arrow" v-if="showArrow">
      <span class="moreText">{{moreText || '更多'}}</span>
      <div class="arrow"></div>
    </div>
  </router-link>-->
  <a class="tit-warp" :href="href" v-if="href">
    <div class="tit-name">{{tit}}</div>
    <div class="tit-arrow" v-if="showArrow">
      <span class="moreText" :class="{'androidHack' : sys === 'Android'}">{{moreText || '更多'}}</span>
      <div class="arrow"></div>
    </div>
  </a>
  <div class="tit-warp" v-else="!href">
    <div class="tit-name">{{tit}}</div>
    <div class="tit-arrow" v-if="showArrow">
      <div class="arrow"></div>
      <div class="arrow arrow2"></div>
      <!--<span class="huan-btn" @click="replace">换一换</span>-->
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        sys: window.sys
      }
    },
    computed: {},
    props: {
      tit: {
        type: String,
        default: ''
      },
      moreText: {
        type: String,
        default: ''
      },
      showArrow: {
        type: Boolean,
        default: true
      },
      href: {
        type: String,
        default: ''
      },
      hf: {
        type: Boolean,
        default: true
      }
    },
    mounted() {
    },
    components: {},
    methods: {}
  }
</script>

<style lang="scss" scoped>
  @import "../../../assets/css/css-var";
  .tit-warp{
    position: relative;
    display: flex;
    align-items: center;//子元素垂直居中
    justify-content: center;
    padding: 1.5rem 1rem 1rem 1rem;
    background: #ffffff;
    font-size: 0;
    .tit-name{
      flex: 1;
      font-size: 1rem;
      color: #2c2c2c;
      font-weight: bold;
      line-height: 1rem;
    }
    .tit-arrow{
      position: relative;
      text-align: right;
      display: flex;
      padding-right: 10px;
      color: #9F9F9F;
      /*line-height: 1;*/
      vertical-align: middle;
      .moreText{
        font-size: .65rem;
        line-height: 1;
        position: absolute;
        top: 50%;
        right: 8px;
        white-space: nowrap;
        transform: translateY(-50%);
      }
      .arrow{
        border-top: 1px solid #9F9F9F;
        border-right: 1px solid #9F9F9F;
        position: absolute;
        display: inline-block;
        border-left-width: 0;
        border-bottom-width: 0;
        width: 6px;
        height: 6px;
        top: 50%;
        right: 0;
        transform: translateY(-50%) rotate(45deg);
      }
      .arrow2{
        right: 8%;
      }
    }
    .androidHack{
      padding-top: 2px;
    }
  }

</style>
