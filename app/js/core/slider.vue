<template>
  <div :class="cname">
    <swiper :options="options"  :not-next-tick="options.notNextTick">
      <swiper-slide v-for="item in items" :key="item.href">
        <router-link :to="{name: item.href}">
          <img :src="item.src" alt="img">
        </router-link>
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
      <div class="swiper -button-prev" slot="button-prev"></div>
      <!-- <div class="swiper-button-next" slot="button-next"></div> -->
      <div class="swiper-scrollbar" slot="scrollbar"></div>
    </swiper>
  </div>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  components: {
    swiper,
    swiperSlide
  },
  props: {
    options: {
      type: Object,
      default() {
        return {
          autoplay: true,
          loop: true,
          pagination: {
            el: ".swiper-pagination"
          },
          notNextTick: false
        };
      }
    },
    items: {
      type: Array,
      default() {
        return [];
      }
    },
    cname:{
      type: String,
      default: ""
    }
  },
  data() {
    return {};
  }
};
</script>

<style lang="scss">
@import "~swiper/dist/css/swiper.css";
</style>

