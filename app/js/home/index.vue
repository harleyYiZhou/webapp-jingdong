<template lang="html">
  <div >
    <heador></heador>
    <hslider></hslider>
    <novice></novice>
    <borrow></borrow>
    <money></money>
    <news></news>
    <service></service>
    <footers></footers>
    <navbars></navbars>
  </div>
</template>

<script>
  import heador from "../public/header.vue";
  import hslider from "./hslider.vue";
  import novice from "./novice.vue";
  import borrow from "./borrow.vue";
  import money from "./money.vue";
  import news from "./news.vue";
  import service from "./service.vue";
  import footers from "../public/footer.vue";
  import navbars from "../public/navbar.vue";

  export default {
    components:{
      heador,
      hslider,
      novice,
      borrow,
      money,
      news,
      service,
      footers,
      navbars
    }
  }
</script>

