<template>
  <div class="main_margin">
    <h4>Course Details</h4>



    <div class="row">
        <div class="col-4">
      
          <h1>{{ this.fullCourse.title }}</h1>
          <p>{{ this.fullCourse.description }}</p>
          <hr>
          <h4>Subjects</h4>
      </div>
      <div class="col-8">

        <div class="acordion">
          <div v-for="(i,index) in this.subjects" :key="index" class="accordion accordion-flush" id="accordionFlushExample">
            <div class="accordion-item">
              <h2 class="accordion-header" :id="`flush-heading${index+1}`" >
                <button class="accordion-button collapsed" type="button" data-bs-toggle="collapse" :data-bs-target="`#flush-collapse${index+1}`" aria-expanded="false" :aria-controls="`flush-collapse${index+1}`">
                 <h3> Tema: {{ index+1 }}. {{ i.SubjectName }}</h3> 
                </button>
              </h2>
              <div :id="`flush-collapse${index+1}`" class="accordion-collapse collapse" :aria-labelledby="`flush-heading${index+1}`" data-bs-parent="#accordionFlushExample">
                <p> {{ i.DescriptionSubject}}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
</div>


  </div>
</template>

<script>
import axios from 'axios';
 export default {
    data(){
        return{
          fullCourse: {

            },subjects:{

            }
        }
    },async created(){

      try {
        const response = await axios.get('https://cursos-online-xavi-s-code-default-rtdb.europe-west1.firebasedatabase.app/Cursos/'+ this.$route.params.id +'.json')
        this.fullCourse=response.data;
        this.subjects= this.fullCourse.Subjects;
        this.subjects=this.subjects.splice(1, this.subjects.length);
        console.log(this.subjects)
      } catch (error) {
          console.log(error)
      }
    
    }
    
}
</script>

<style lang="scss" scoped>
.main_margin{
  margin-top: 10rem;
}

</style>