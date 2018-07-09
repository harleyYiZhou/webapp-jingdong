<template>
  <panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <ul>
        <li v-for="item in items" :key="item.href">
          <dl>
            <dt>{{item.title}}
              <span>{{item.sub}}</span>
            </dt>
            <dd>{{item.rate}}</dd>
            <dd>{{item.desc}}</dd>
          </dl>
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
          href: "Home",
          title: "定期理财",
          sub: "理财首选",
          rate: "5.60%",
          desc: "历史年化回报率"
        },
        {
          href: "Home",
          title: "定期理财",
          sub: "理财首选",
          rate: "5.60%",
          desc: "历史年化回报率"
        },
        {
          href: "Home",
          title: "定期理财",
          sub: "理财首选",
          rate: "5.60%",
          desc: "历史年化回报率"
        },
        {
          href: "Home",
          title: "定期理财",
          sub: "理财首选",
          rate: "5.60%",
          desc: "历史年化回报率"
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
  .content {
    ul {
      @include flex(row);
      &:after{
        content: '';
        width: 100%;
        height: 0;
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        display: block;
        position: relative;
        top: -208px;
      }
      li {
        width: 50%;
        padding: 34px 16px;
        box-sizing: border-box;
        position: relative;
        &:after {
          content: "";
          width: 1px;
          height: 136px;
          display: block;
          position: absolute;
          top: 50%;
          right: 0;
          margin-top: -68px;
          border-right: 1px solid #eee;
        }
        &:nth-child(2n) {
          &:after {
            display: none;
          }
        }
        dt {
          font-size: 30px;
          height: 42px;
          color: #333;
          span {
            font-size: 22px;
            color: #ff5155;
            border: 1px solid #ff5155;
            padding: 0 8px;
            margin-left: 2px;
          }
        }
        dd {
          white-space: nowrap;
          text-overflow: ellipsis;
          overflow: hidden;
          &:nth-child(2) {
            font-size: 44px;
            height: 55px;
            line-height: 55px;
            color: #ff5155;
            font-weight: 700;
          }
          &:nth-child(3) {
            font-size: 24px;
            height: 34px;
            line-height: 34px;
            color: #999;
          }
        }
      }
    }
  }
}
</style>
