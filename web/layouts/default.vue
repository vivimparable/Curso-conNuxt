<template>

    <div>
        <nabar/>
        <Nuxt/>
    </div>
  
</template>

<script>
import nabar from '@/components/defaultView/navbar.vue'
export default {

  components:{
    nabar
  },

    head(){
    return{
      title:'Xavi',
      meta:[{
        name:'description',
        content:'Website about me'
      }],
      htmlAttrs:{
        lang:'en'
      }, link: [
        { rel: 'stylesheet', href: '/bootstrap/bootstrap.min.css' }
      ],
      script: [
        { src: "/bootstrap/bootstrap.bundle.min.js", type: "text/javascript"}
      ]
    }
  }
}
</script>

<style lang="scss">
//box sizing//
*,
*::before,
*::after {margin: 0;
    padding: 0;
    box-sizing: inherit;
}  

html {
    font-size: 62.5%;
    box-sizing: border-box;
}



//Global Css//
  ul{
    list-style: none;
    li{
      font-size: 1.5rem;
    }
  }
  p{
    font-size: 1.5rem;
    
  }
  h1{
    font-size: 4rem;
  }
  h2{
    font-size: 3.4rem;
  }
  h3{
    font-size: 2.9rem;
  }

</style>