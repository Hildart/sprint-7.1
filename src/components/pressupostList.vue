<template>
    


    <div class="col" >
        <button @click="$emit('ordenAlfabetico')" class="col-3 btn btn-success border-dark mb-2">Orden alfabetico</button>
        <button @click="$emit('ordenFecha')" class="col-3 btn btn-success border-dark mb-2">Ordenar fecha</button>
        <button @click="$emit('ordenImporte')" class="col-3 btn btn-success border-dark mb-2">Ordenar importe</button>
        <button @click="$emit('reinicio')" class="col-3 btn btn-success border-dark mb-2">Reiniciar orden</button>
        
        

        <ul v-for="(presu, index) in listaPresupuestos" :key="index">
            <div class="border border-dark rounded">
                <p class="m-2">Presupuesto {{ presu.id }}: {{ presu.Presupuesto }}</p>
                <p class="m-2">Nombre del cliente: {{ presu.Cliente }}</p>
                <p class="m-2">Precio total: {{ presu.Total }}€</p>
                <p class="m-2">{{ presu.Fecha }}</p>
            </div>
        </ul>
    </div>

    
    


</template>

<script setup>

const props = defineProps({
    listaPresupuestos: Array,
});


</script>