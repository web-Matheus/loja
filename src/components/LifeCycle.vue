<template>
    <div>
        <h3>Essa é uma mensagem dinâmica alterada do 
        lifecycle created : {{msg}}</h3>
        <h4>{{count}}</h4>
        <p v-if="job"> Essa pessoa tem trabalho</p>
        <p v-else>Essa pessoa esta em busca de um emprego</p>
    </div>
</template>
<script>
export default {
    name:"LifeCycle",
    data(){
        return{
            msg:"Sem msg",
            count:0,
            job:false
        }
    },
    created(){
        setTimeout(()=>{
            this.msg = "Matheus"
        },1000)
    // método do lifecycle hook é ativado após um intervalo
    // de um seg, e muda msg para o valor Matheus 
    },
    // created(){
    //     setInterval(()=>{
    //         this.count++
    //     },1000)
    // }
}
</script>