<template>
  <panel title="新品推荐" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.more">更多尖货 ></div>
    </section>
    <swiper :options="options" :items="items" cname="swiper"></swiper>
  </panel>
</template>

<script>
import panel from "../core/panel.vue";
import swiper from "../core/slider.vue";

export default {
  components: {
    panel,
    swiper
  },
  data() {
    return {
      options: {
        slidesPerView: 2.3,
        spaceBetween: 30,
        freeMode: true
      },
      items: [
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t13963/267/2355123229/48850/254f797a/5a3c59aeN9cb550f6.jpg?width=335&height=421"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t13021/306/1996997425/21953/bda69db3/5a2f6a17N9da099b1.jpg?width=335&height=421"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t14125/310/1997192193/46667/3c910f8b/5a2f6a36Nad95b650.jpg?width=335&height=421"
        },
        {
          href: "Home",
          src:
            "//img12.360buyimg.com/jrpmobile/jfs/t15784/188/381232069/39444/8878571d/5a2f6a4aNbd5a574c.jpg?width=335&height=421"
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
  .content {
    position: relative;
    .more {
      position: absolute;
      top: -70px;
      right: 20px;
      font-size: 28px;
      color: #999;
    }
  }
}
</style>

<style lang="scss">
.swiper {
  padding: 0 24px;
  .swiper-slide {
    box-sizing: border-box;
    img {
      width: 100%;
    }
  }
}
</style>
