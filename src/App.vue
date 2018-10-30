<template>
  <div id="app">
    <keep-alive exclude="Detail">
      <router-view/>
    </keep-alive>
  </div>
</template>

<script>

  export default {
  name: 'App',
    data(){
    return{
    }
    },
    components:{
    }
}
</script>

<style>
  *{
    padding: 0;
    margin: 0;
  }

#app {


}
</style>
