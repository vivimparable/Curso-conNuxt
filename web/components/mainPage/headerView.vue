<template>
    <header class="header__image ">
      <div class="header__image__backColor">
      <div class="d-flex flex-column">
        <div>
          <h1 class="text-light">Welcome to Xavi's Courses</h1>
        </div>
  
        <div>
            <h4 class="text-light">
            Current courses: 0
            </h4>
        </div>
      </div>
      </div>
      
    </header>
  </template>
  
  <script>
  export default {
  
  }
  </script>
  
  <style lang="scss" scoped>
  
  .header__image{
    height: 76vh;
    background-image: url('@/assets/img_header.jpg') ;
    .header__image__backColor{
      background-color: rgb(0, 0, 0,0.4);
      div{
      height: 75vh;
      display: flex;
      justify-content: center;
      align-items: center;
      h1{
        border-bottom: 0.4rem solid white;
      }
      
    }
    }
    
  }
  
  </style>