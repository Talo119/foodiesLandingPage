<template>
  <div>
      <div class="row">
            <div class="col-md-5">
                <h3 class="text-center">Estamos para ti</h3>
                <div class="btn-group p-0 m-0 w-100" role="group" aria-label="Basic example">
                    <button type="button" 
                            :class="tipo_pedido === 'takeaway' ? 'btn btn-dark' : 'btn btn-outline-dark'" 
                            @click.prevent="tipoPedido('takeaway')"
                    >
                        <i class="fas fa-hamburger mr-3"></i>
                        Para llevar
                    </button>
                    <button type="button" 
                            :class="tipo_pedido === 'delivery' ? 'btn btn-dark' : 'btn btn-outline-dark'" 
                            @click.prevent="tipoPedido('delivery')"
                    >
                        <i class="fas fa-truck mr-3"></i>
                        Domicilio
                    </button>                    
                </div>
                
                <div class="input-group mb-3 mt-2">
                    <div class="input-group-prepend">
                        <span class="input-group-text" id="basic-addon1">
                            <i class="fas fa-search"></i>
                        </span>
                    </div>
                    <input  type="text" 
                            class="form-control" 
                            placeholder="Buscar nombre o direccion" 
                            aria-label="Username" 
                            aria-describedby="basic-addon1"
                            v-model="search"
                    >
                </div>
                <template v-if="locationsFiltrados.length > 0">
                    <div class="list-group">
                        <button type="button"
                                v-for="location in locationsFiltrados" 
                                :key="location.id" 
                                class="list-group-item list-group-item-action"
                        >                        
                            <strong class="d-block">{{location.name}}</strong>
                            <small class="d-block">Abierto de {{location.opening_time}} - {{location.closing_time}}</small>
                            <small class="d-block">{{location.address}}</small>
                        </button>           
                    </div>
                </template>
                <template v-else>
                    <img class="no-results" src="../assets/imagenes/errorSearch - desktop.png" alt="Locations">    
                </template>
                

                
            </div>
            <div class="col-md-7">
                <img class="sucursales-img d-none d-sm-block" src="../assets/imagenes/sucursales/Rectangle 4.png" alt="Locations">
            </div>
      </div>
      
  </div>
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            tipo_pedido: 'takeaway',
            locations:[],
            search:''
        }
    },
    created () {
        this.getLocations('takeaway');
    },
    computed: {
        locationsFiltrados(){
            
            if (this.search == null) {
                //this.itemsFiltrado = this.items;
                return this.locations;
            } else {
                return this.locations.filter(location =>{
                    if (location.name.includes(this.search) || location.address.includes(this.search)) {
                        return true;
                    }
                });
            }
            
            
        },
    },
    methods: {
        tipoPedido(tipo) {
            if(tipo === 'takeaway'){
                this.tipo_pedido = 'takeaway';
            } else {
                this.tipo_pedido = 'delivery';
            }

            this.getLocations(this.tipo_pedido);
            
        },

        getLocations(tipoPedido){            
            var locationsArray =[];
            axios.get('api/locations?type=' + tipoPedido)
            .then(response =>{                
                this.locations = response.data.data;
            }).catch(function(error){
                console.log(error);
            })         
            
        }

        
    },
}
</script>

<style>
    .sucursalees-img{
        position: absolute;
        width: 824px;
        height: 609px;
        left: 676px;
        top: 1519px;

        background: url('../assets/imagenes/sucursales/Rectangle 4.png');
    }
    .no-results{
        position: relative;
        width: 566px;
        height: 341px;
    }
    
</style>