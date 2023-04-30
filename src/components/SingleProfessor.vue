<template>
    

    <div>

                        <h2>{{professor.name}}</h2>
                        <h4>Phone Number: {{professor.phoneNumber}}</h4>
                        <h4>Mail Id: {{professor.mailId}}</h4>
                        <h4>Courses Taught: {{professor.courses}}</h4>
                        <a :href="professor.portfolioLink">See full profile</a>
                       
                       
                    
    </div>
</template>

<script>



export default{
    name: 'SingleProfessor',
    props:{
        professor: Array
    }
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    
    color: black;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;

}
div a{
    color:white;
}




</style>