<template>
  <panel title="生活服务" :cname="$style.panel">
    <section :class="$style.content">
      <ul>
        <li v-for="item in items" :key="item.href">
          <img :src="item.src" alt="">
          <p>{{item.title}}</p>
          <p v-if="item.sub!==''">{{item.sub}}</p>
        </li>
      </ul>
    </section>
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
          src:
            '//img12.360buyimg.com/jrpmobile/jfs/t4375/104/1184122472/3976/89741da4/58be8a6eNf10193d0.png?width=135&height=135"',
          title: "慧加油",
          sub: ""
        },
        {
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t4747/185/1901740991/5892/1383fb93/58f57851N17ee6993.jpg?width=132&height=132",
          title: "小白信用",
          sub: "全新升级"
        },
        {
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3241/234/8044685271/3713/7b29f77f/58be89c8Nb9d41295.png?width=135&height=135",
          title: "信用卡还款",
          sub: ""
        },
        {
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3172/259/7993557249/4351/fd082707/58be8a81Nd7716a06.png?width=135&height=135",
          title: "卡转让",
          sub: ""
        },
        {
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3085/320/8107659086/4344/cdbba2dd/58be8acfNdadcaf00.png?width=135&height=135",
          title: "定期还款",
          sub: ""
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
  ul {
    @include flex(row);
    justify-content: space-around;
    padding-bottom: 40px;
    li {
      text-align: center;
      img {
        width: 90px;
        height: 90px;
      }
      p {
        font-size: 26px;
        color: #666;
        margin-top: 12px;
        text-overflow: ellipsis;
        overflow: hidden;
        white-space: nowrap;
        &:nth-child(3) {
          color: #ff801a;
        }
      }
    }
  }
}
</style>
