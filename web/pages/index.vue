<template>
    <div class="main">
      <div class="container-custom">
          <div class="row main__home align-items-center ">
              <div class="col-6 main__home__header  " >
                  <p>Xavi's Code</p>
                  
                  <h1>Welocme Xavi's courses platform</h1>
                  <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Culpa nobis fugit incidunt deleniti! Nihil sed incidunt nostrum nulla nobis, harum iste praesentium. Fuga, temporibus laudantium! Obcaecati nisi et impedit, magni ducimus harum voluptates architecto minus dignissimos aliquid unde provident quis perferendis commodi fugiat quibusdam iure maiores libero totam, ullam illo molestias incidunt. Rerum facilis maxime modi magnam quidem molestiae quas accusamus? Excepturi corrupti ex alias! Voluptate recusandae nobis tempore nemo soluta quo corporis! Maiores, nihil facilis vero ad earum amet laborum consequatur aspernatur! Commodi labore quidem fugiat soluta, quis odit dicta? Voluptates tenetur perferendis odit impedit cum nulla consectetur labore?</p>
                    <button @click="ContentReplace('mainPage')"  class="btn btn-outline-light pb-0"><p>See the project</p> </button>
                    <button @click="ContentReplace('aboutMe')" class="btn btn-outline-light pb-0"><p>
                     About me 
                    </p>
                      </button>
              </div>
              <div class="col-6 lista ">
                  <ul class="text-light text-center ">
                    <li class="lista--lista1">Find</li>
                    <li class="lista--lista2">Start</li>
                    <li class="lista--lista3">Learn</li>
                  </ul>
              </div>
          </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'IndexPage',
  methods:{
    ContentReplace(route){
          this.$router.push({name:route})
    }
  }
  
}
</script>

<style lang="scss" scoped>

@import '~/SassFolder/GlobalSass.scss';

//List//
.lista{
  text-align: right;
    ul{
    list-style-type: none;
    display: inline-block;
      li{ 
        padding: 1rem;
        margin-top: 2rem;
        color: $mainColor;
      }
  }
}

//Container and back image//
.container-custom{
  width: 80%;
  margin: auto;
}
.main{
  background-image: url('@/assets/mainImage.jpg');
  background-size: cover; 
  height: 100vh;
}


.main__home {
  height: 100vh;
  //animations//
  .main__home__header{
    @include mainAnmation;
  }
  
}

ul  {
  .lista--lista1{
    @include animacion(1s)
  }

  .lista--lista2{
    @include animacion(2s)
  }

  .lista--lista3{
    @include animacion(3s)
  }
  
}




</style>
