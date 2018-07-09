<template>
  <panel title="navbar" :class="$style.panel">
    <ul>
      <li v-for="item in items" :key="item.href">
        <router-link :to="{'name': item.href}">
          <img :src="item.src" alt="">
          <p>{{item.title}}</p>
        </router-link>
      </li>
    </ul>
  </panel>
</template>

<script>
import panel from "../core/panel.vue";

export default {
  components: {
    panel
  },
  data(){
    return {
      items: [
        {
          href: 'Home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t3451/188/644771475/2428/800d7cb7/580f2435Nbfaa8055.png?width=66&height=66',
          title: '首页'
        },
        {
          href: 'Home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t3811/55/345433999/2930/116d3dd1/580f1e25N028a1f2c.png?width=66&height=66',
          title: '理财'
        },
        {
          href: 'Home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t3343/179/621044750/1484/5af6b11a/580f50e4N005181d0.png?width=66&height=66',
          title: '白条'
        },
        {
          href: 'Home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t3604/98/635506544/2317/443d3a51/580f240aNbee3dcc4.png?width=66&height=66',
          title: '众筹'
        },
        {
          href: 'Home',
          src: '//img12.360buyimg.com/jrpmobile/jfs/t3340/68/639059082/2591/800e2d6b/580f51cdN4caf20b2.png?width=66&height=66',
          title: '我的'
        }
      ]
    }
  }
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
  @include panel;
  height: 100px;
  width: 100%;
  position: fixed;
  margin: 0px;
  left: 0px;
  bottom: 0;
  right: 0;
  z-index: 100;
  >h4{
    display: none;
  }
  ul{
    @include flex(row);
    justify-content: space-around;
    li{
      img{
        width: 44px;
        height: 44px;
        margin: 12px auto 6px;
      }
      p{
        font-size: 22px;
        color: #656565;
      }
      a{
        text-decoration: none;
      }
    }
  }
}

</style>
