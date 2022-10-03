<template>
    <div class="row">
        <div class="col-lg-8">
            <h4>{{titulo}}</h4>
            <table class="table">
                <thead>
                    <tr>
                        <th>N°</th>
                        <th>Modelo</th>
                        <th>Descripcion</th>
                        <th>Precio</th>
                        <th>% de descuento</th>
                        <th>Reputacion</th>
                        <th>stock Disponible</th>
                        <th>Marca</th>
                        <th>Categoria</th>
                        <th>Imagen</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(u,index) of lista_productos" v-bind:key="index">
                        <td>{{index}}</td>
                        <td>{{u.title}}</td>
                        <td>{{u.description}}</td>
                        <td>{{u.price}}</td>
                        <td>{{u.discountPercentage}}</td>
                        <td>{{u.rating}}</td>
                        <td>{{u.stock}}</td>
                        <td>{{u.brand}}</td>
                        <td>{{u.category}}</td>
                        <td><img :src=u.thumbnail class="img-fluid" style="width:20rem"></td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
</template>
<script>
/* eslint-disable */
import {ref} from 'vue'
export default {
    name:'FormProdcuto',
    setup() {    
        //sector de variables
        let nombre = ref('')
        let lista_productos = ref([])
        let titulo = ref('Lista de Prodcutos')
        //sector de funciones
        async function consumir_api2(){
            const productos = await fetch('https://dummyjson.com/products')
            const datos = await productos.json()
            lista_productos.value = await datos.products           
        }
        return{
            nombre,
            consumir_api2,
            lista_productos,
            titulo
        }
    },
    created(){
        this.consumir_api2()
    }
}
</script>