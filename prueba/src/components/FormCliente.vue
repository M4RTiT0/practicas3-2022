<template>
    <div class="row">
        <div class="col-lg-4">
            <h2> Probando Componentes </h2>
            <div class="mb-3">
                <label class="form-label">Nombre</label>
                <input v-model="nombre" class="form-control" type="text">
            </div>
            <button @click="mostrar()" class="btn btn-success">Aceptar</button>
        </div>
    </div>
</template>
<script>
/* eslint-disable */
import { ref } from 'vue'
export default {
    name:'FormCliente',
    setup() {

        //sector de variables
        let nombre = ref('')

        //sector de funciones
        function mostrar(){
            alert(nombre.value)
        }

        return{
            nombre,
            mostrar
        }

    },
}
</script>