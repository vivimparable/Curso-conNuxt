<template>
    
    <nav v-if="this.$route.path!='/'"  class=" navbar fixed-top navbar-dark bg-dark">
  <div class="container-fluid ">
    <a class="navbar-brand" @click="Back()">
      <div v-if="this.sizeWindows>785">
          <h1>Xavi's Code</h1> 
      </div>
      <div v-else>
        <h1>XC's</h1> 
      </div>
    </a>
    <div>
      <ul class="d-flex ">
        <li class="nav-item">
          <nuxt-link class="nav-link" to="/posts">Posts</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" to="/aboutMe">About</nuxt-link>
        </li>
      </ul>
    </div>
  </div>
</nav>        
</template>

<script>
export default {
name:'navBar',
data(){
  return{
    sizeWindows:null
  }
}, created(){
    if (process.browser){
      this.sizeWindows=window.innerWidth;
    }
  },watch:{
    sizeWindows(){
      window.addEventListener('resize', (e)=>{
        this.sizeWindows = e.target.innerWidth
      })
    }
  },methods:{
    Back(){
      this.$router.push({path:'/'})
    }
  }

}
</script>

<style>

</style>