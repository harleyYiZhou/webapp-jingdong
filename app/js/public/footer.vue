<template>
  <panel title="公司信息" :class="$style.panel">
    <ul>
      <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252" alt="">
      <li>
        <div v-for="item in items" :key="item.href">
          <img :src="item.src" alt="">
          <p>{{item.title}}</p>
        </div>
      </li>
      <li>Copyright © 2004-2017 京东JD.com 版权所有</li>
      <li>投资有风险，购买需谨慎</li>
      <li>京东金融平台服务协议</li>
    </ul>
  </panel>
</template>

<script>
import panel from "../core/panel.vue";

export default {
  components: {
    panel
  },
  data() {
    return {
      items: [
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108",
          title: "客户端"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108",
          title: "触屏版"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108",
          title: "电脑版"
        }
      ]
    };
  }
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel {
  @include panel;
  margin-top: 20px;
  margin-bottom: 100px;
  >h4{
    display: none;
  }
  ul {
    text-align: center;
    background: #f5f5f5;
    img {
      width: 100%;
    }
    li {
      &:nth-child(2) {
        @include flex(row);
        justify-content: space-around;
        color: red;
        padding: 20px 0;
        img {
          width: 90px;
          height: 90px;
        }
        p {
          font-size: 26px;
          color: #999;
          margin-top: 12px;
          text-overflow: ellipsis;
          overflow: hidden;
          white-space: nowrap;
        }
      }
      &:nth-child(n + 3) {
        font-size: 24px;
        color: #999;
        height: 40px;
        line-height: 40px;
        border-top: 1px solid #ddd;
        padding: 24px 0;
      }
      &:last-child{
        border-bottom: 1px solid #ddd;
      }
    }
  }
}
</style>
