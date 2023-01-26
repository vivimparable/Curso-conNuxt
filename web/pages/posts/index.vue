<template>
  <div>
    <h1>Current Courses</h1>
    <div >
       
        <PostsView 
        v-for="i of data" :key="i.id" :id="i.id"  :title="i.title" :type="i.type" :description="i.description" :level="level"/>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
import PostsView from '~/components/postsView/PostsView.vue'
export default {
    components:{
        PostsView
    },
    data(){
        return{
            data:[]
        }
    },
    async created(){
        try {
            const resp =  await axios.get('https://cursos-online-xavi-s-code-default-rtdb.europe-west1.firebasedatabase.app/Cursos.json')
        this.data=resp.data;
        console.log(this.data)
        } catch (error) {
            console.log(error)
        }
       
    }
}
</script>

<style lang="scss" scoped>


div { 
  padding-top: 6.9rem; 
 
}
</style>