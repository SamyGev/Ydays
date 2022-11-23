<template>
    <div>
        <h1>Bonjour toto</h1>
        <input type="text" v-model="msg">
        <div v-for="lampe in lampes" :key="lampe.lampe">
            <h1>{{lampe.lampe}}</h1>
            <h2>{{lampe.prix}}</h2>
            <span>{{lampe.id}}</span>
        </div>
        

        <titi :msg="msg"></titi>
    </div>


</template>

<script>
import titi from '../components/HelloWorld.vue';
import lampe from '../../lampes.json'
export default { 
    title: 'coucou',
    components: {titi},
    data(){
        return {
            msg:"",
            lampes:lampe
        }
}
}
</script>

<style>

</style>