<template>
  <div class="detail-page">
    <h5>{{ip}}</h5>
    {{JSON.stringify(detail)}}
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
      const detail = await $axios.$get('/talentMap/creativePlatform?timestamp=1595839686961');
      const ip = await $axios.$get('http://icanhazip.com');

      console.log(detail)
      return {detail, ip}
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
