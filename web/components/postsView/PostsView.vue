<template>


<div class="row row-cols-1 row-cols-md-3 g-4 justify-content-center"> 
    <div class="col-12">
    <div class="card h-100">
          <div class="">
          <img v-if="this.type == 'programming'" src='@/assets/code.jpg'  class="card-img-top" alt="...">
          <img v-if="this.type == 'design'" src='@/assets/design.png'  class="card-img-top" alt="...">
          <img v-if="this.type == 'marketing'" src='@/assets/marketing.jpg'  class="card-img-top" alt="...">

          <div class="">
            <h2 class="">{{ title }}</h2>
            <p class="">{{description }}</p>
          </div> 

          <nuxt-link :to="'/posts/'+ id"> Click </nuxt-link>
        </div>
    </div>
  </div>
</div>

  
</template>

<script>
import imagens from '@/assets/code.jpg'
export default {
name:'posts',
props:['id','title','description','type'],
components:{
  imagens
}
}
</script>

<style>

</style>