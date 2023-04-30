<template>
<div>
    <h1> {{heading}} </h1>
  
</div>
</template>

<script>

export default{ // Exporting Default Object
    name: 'MyHeader',
    props:{ 

        heading:String
    }
}

</script>

<style scoped>

div{
    padding: 30px;
    text-align: center;
    height:100px;
    color: white;
    background-color :rgb(7, 30, 84);
}

</style>