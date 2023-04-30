<template>
   
    
    <div v-for="professor in professors" :key="professor.id" >

     
       <SingleProfessor :professor="professor" />

    </div>

</template>
<script>
import SingleProfessor from './SingleProfessor.vue';

export default {
    name: 'ProfessorBox',
    props:{
        professors: Array
    },
    components:{
    SingleProfessor
}
    
}
</script>
<style scoped>
div{
    background-color:rgb(26, 81, 210);
    color:white;
    text-decoration: none;

}


</style>
