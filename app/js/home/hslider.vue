<template>
  <article class="">
    <Slider :cname="$style.slider" :items="items"></Slider>
    <section :class="$style.list">
      <div :class="$style.item" v-for="item in enters" :key="item.href">
        <router-link :to="{name: item.href}">
          <img :src="item.src" :alt="item.title">
          <h4>{{item.title}}</h4>
        </router-link>
      </div>
    </section>
  </article>
</template>

<script>
import Slider from "../core/slider.vue";

export default {
  components: {
    Slider
  },
  data() {
    return {
      items: [
        {
          href: "Home",
          src:
            "https://img12.360buyimg.com/jrpmobile/jfs/t21427/315/1947457000/48815/dc123010/5b3f482eN0a7e722b.jpg?width=750&height=320"
        },
        {
          href: "Home",
          src:
            "https://img12.360buyimg.com/jrpmobile/jfs/t19990/237/1804913220/36610/e0f6b3e8/5b3f4808N5b4880b9.jpg?width=750&height=320"
        },
        {
          href: "Home",
          src:
            "https://img12.360buyimg.com/jrpmobile/jfs/t19990/237/1804913220/36610/e0f6b3e8/5b3f4808N5b4880b9.jpg?width=750&height=320"
        },
        {
          href: "Home",
          src:
            "https://img12.360buyimg.com/jrpmobile/jfs/t21427/315/1947457000/48815/dc123010/5b3f482eN0a7e722b.jpg?width=750&height=320"
        }
      ],
      enters: [
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
          title: "优惠券"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
          title: "领红包"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t4393/329/2180608902/13217/c88c0cec/58ec9dcdN1534e2d7.png?width=132&height=132",
          title: "抢钢蹦"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
          title: "白条提额"
        }
      ],
      slider: "slider"
    };
  }
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.slider {
  margin-top: 120px;
  img {
    width: 100%;
  }
}
.list {
  @include list(row);
  background: #fff;
  padding-top: 40px;
  padding-bottom: 20px;
  justify-content: space-around;
  a {
    text-decoration: none;
  }
  .item {
    text-align: center;
    img {
      // display: inline-block;
      height: 90px;
      width: 90px;
    }
    h4 {
      font-size: 26px;
      margin-top: 12px;
      color: #666;
    }
  }
}
</style>