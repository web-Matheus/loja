<template>
<!-- todo template deve retornar apenas um elemento por isso esta
envolvida em div -->
<!-- metodo data() serve para passar dados para o 
template -->
    <div>
        <h1>Olá, vue</h1>
    <p>Meu nome é {{nome}} e minha idade {{idade}}</p>
    </div>
</template>

<script>

export default{
    name:'Comp',
    data(){
        return{
         nome:"Matheus",
         idade:"21"  
        }
    }
}
</script>
