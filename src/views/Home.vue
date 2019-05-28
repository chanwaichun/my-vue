<template>
  <div class="home">
    <p>HelloWorld</p>
    <p>{{this.$store.state.username}}</p>
    <HelloWorld :msg="message" />
  </div>
</template>
<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'home',
  data()
  {
    return({
       message:"helloworld"
    })
   
  },
  components: {
    HelloWorld,
  },
};
</script>
<style lang="scss" scoped>
.home
{
  $color:red;
  p{
    color:$color;
  }
}
</style>
