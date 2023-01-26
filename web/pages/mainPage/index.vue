<template>
  <div>
    <headerView/>
    <typeCourses/>
    <separator ad="'The more you learn, the wiser you get'" />
 
    <footerNav />
  </div>
  
</template>

<script>
import headerView from '@/components/mainPage/headerView.vue';
import typeCourses from '@/components/mainPage/typeCourses.vue';
import separator from '@/components/mainPage/separator.vue'
import footerNav from '~/components/mainPage/footerNav.vue'

export default {
components:{
  headerView,
  typeCourses,
  separator,
  footerNav
}
}
</script>

<style lang="scss" scoped>
div { 
  padding-top: 6.9rem; 
 
}

</style>