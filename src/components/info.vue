<template>
   <div>
    <h2>Componente sobre diretivas/argumentos</h2>
    <a :href="meu_port" target="_blanck">Acesse meu portfolio</a>
    <ul>
        <li v-show="mostrar_list" v-for="(itens,index) in backend_itens" 
        v-bind:key="index">{{itens}}</li>
    </ul>
    <button @click="show_list">click</button>
    <ul>
        <li v-for="itens in frontend_itens" :key="itens.id">
            {{itens.language}}
        </li>
    </ul>
    <form action="" @submit="enviar_form($event)">
        <input type="text" v-model="form_name">
        <input type="text" v-model="form_email">
        <input type="submit">
    </form>
   </div>
</template>
<script>
export default {
    name:"Info",
    data() {
       return{
           mostrar_list:true,
           meu_port:"https://web-matheus.github.io/matheus-site/",
           backend_itens:['javascript','php','python','java','c#'],
           frontend_itens:[
               {id:1,language:"html"},
               {id:2,language:"css"},
               {id:3,language:"vue"}
           ],
           form_name:"",
           form_email:""
       } 
    },
    methods:{
        //método para mostrar/não mostrar lista
        show_list(){
            this.mostrar_list = !this.mostrar_list
        },
        //método para captar valor o formulário
        enviar_form(e){
            e.preventDefault()
            const name = this.form_name;
            const email = this.form_email;
        }
    }
}
</script>