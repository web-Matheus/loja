<template>
    <div>
        <button @click="ativar">Click</button>
        <span v-show="ativou">Ativado!</span>
    </div>
</template>

<script>
export default {
    name:"Reutilização",
    data(){
        return{
            ativou:false
        }
    },
    methods:{
        ativar(){
            this.ativou = !this.ativou
        }
    }
}
</script>

<style scoped>
    div{
        margin: 100px;
    }
</style>