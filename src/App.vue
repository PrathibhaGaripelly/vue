<template>

  <!--Step 3 use the component-->
  <MyHeader heading="University Of New Haven Computer Science Graduate Staff"/> 
  <ProfessorBox :professors="professors" />
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import ProfessorBox from './components/ProfessorBox.vue'


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    ProfessorBox
  },
  data(){
    return {
      professors: []
    }
  },
  methods:{
    //promoises
    async fetchprofessors(){
      const res = await fetch('http://localhost:5959/professors');
      const data = await res.json()
      console.log(data)
      return data;
    }
  },
  async created(){
      this.professors = await this.fetchprofessors();
  }

  // data() => this.data books
  // method => this.method => fetchbook
  // life cycle hooks created() => call our method here

}
</script>


<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 400px;
  margin: 30px auto;
  overflow: auto;
  min-height: 400px;
  border: 0.3em solid rgb(48, 48, 49);
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.3em;
  background-color: rgb(151, 181, 214);

}


</style>
