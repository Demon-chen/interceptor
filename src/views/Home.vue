<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import {request} from '../components/request'
export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  mounted() {
      request({
        url:'/home/multidata',
      }).then(res=>{
        console.log(res);
      })
  },
}
</script>
