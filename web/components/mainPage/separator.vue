<template>
  <div>
    <div class="backgroundImage">
        <h1>{{ ad }}</h1>
        <button class="btn btn-outline-light pb-0 mt-5"> 
            <p>
               See the full courses  
            </p>
            </button>
    </div>
   
  </div>
</template>

<script>
export default {
props:{
    ad:{
        type:String
    }
}
}
</script>

<style lang="scss" scoped>
    div{
        height: 35vh;
        background: rgb(158,200,130);
        background: linear-gradient(90deg, rgba(158,200,130,1) 4%, rgba(53,168,28,1) 57%, rgba(8,136,0,1) 83%);
        .backgroundImage{
            height: 35vh;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
        }
    }
</style>