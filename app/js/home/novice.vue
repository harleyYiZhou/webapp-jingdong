<template>
  <panel title="新手特权" :class="$style.panel">
    <section :class="$style.content">
      <div :class="$style.item">
        <h4>下载APP
          <span :class="$style.red">送888元红包</span>
        </h4>
        <p :class="$style.gray">新手专享</p>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132" alt="">
      </div>
      <div :class="$style.item">
        <ul>
          <li>
            <img :class="$style.right" src="//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132" alt="">
            <h4 :class="$style.red">领128元新手红包</h4>
            <p :class="$style.gray">立即开通</p>
          </li>
          <li>
            <img :class="$style.right" src="//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132" alt="">
            <h4>打白条
              <span :class="$style.red">免利息</span>
            </h4>
            <p :class="$style.gray">立即开通享好礼</p>
          </li>
        </ul>
      </div>
    </section>
  </panel>
</template>

<script>
import panel from "../core/panel.vue";

export default {
  components: {
    panel
  }
};
</script>

<style lang="scss" module>
@import "../../css/element.scss";

.panel {
  @include panel;
  > h4 {
    border-bottom: 1px solid #ddd;
  }
  .content {
    @include list(row);
    .item {
      width: 50%;
      box-sizing: border-box;
      &:first-child {
        padding: 32px 20px;
        text-align: center;
        border-right: 1px solid #ddd;
        img {
          width: 132px;
          height: 132px;
          margin: 20px auto 0;
        }
      }
      p {
        margin-top: 6px;
      }
      h4 {
        font-size: 26px;
        line-height: 40px;
        text-overflow: ellipsis;
        white-space: nowrap;
        overflow: hidden;
      }
      .red {
        color: #f00;
      }
      .gray {
        color: #999;
        font-size: 24px;
      }
      ul {
        width: 100%;
        li {
          width: 100%;
          height: 144px;
          padding: 32px 28px;
          box-sizing: border-box;
          img {
            width: 80px;
            height: 80px;
            float: right;
          }
          &:first-child {
            border-bottom: 1px solid #ddd;
          }
        }
      }
    }
  }
}
</style>
