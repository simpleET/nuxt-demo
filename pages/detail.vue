<template>
  <div class="detail-page">
    <h5>{{ip}}</h5>
    {{JSON.stringify(detail)}}
    {{JSON.stringify(home_page)}}
    <ul>
    </ul>a
  </div>
</template>

<script>
  import axios from 'axios';

  export default {
    data() {
      return {
        title: '详情页',
      }
    },
    async asyncData({$axios}) {
      console.log(343443)
      // const detail = await $axios.$get('http://192.168.20.116:819/api/talentMap/creativePlatform?timestamp=1595839686961');
      // const detail = await $axios.$get('/talentMap/creativePlatform?timestamp=1595839686961');
      // const ip = await $axios.$get('http://icanhazip.com');
      const home_page = await $axios.$get('https://www.devio.org/io/flutter_app/json/home_page.json');// 别人的接口

      console.log(home_page)
      return {home_page}
      // console.log(detail,home_page)
      // return {detail, ip,home_page}
    },
  }
</script>
<style scoped>
  ul {
    display: block;
    border: 1px solid red;
  }
  li {
    color: blue;
  }

</style>
