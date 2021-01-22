<template>
    <div class="text-white">
      <div class="row bg-dark">
          <div class="col-12 text-center">
              <h4 class="d-block mt-4 mb-2">Cuentanos tu experiencia</h4>
              <p class="d-block m-0">
                Don't miss out on our great offers & Receive deals from all our                
              </p>
              <p class="m-0">top restaurants via e-mail.</p>
          </div>
          
      </div>

      <div v-if="alert.show" class="row bg-dark">
          <div class="col-12">
              <div :class="alert.tipo  + ' mt-2'" role="alert">
                Error: {{alert.mensaje}}
              </div>
          </div>
      </div>

      <div class="row bg-dark">
        
        <div class="col-md-5 mt-4">
            <div class="form-group">
                <label for="txtNombre">Nombre y Apellido</label>
                <input  type="text" 
                        class="form-control bg-transparent text-white" 
                        id="txtNombre" 
                        v-model="mensaje.name"
                >
            </div>
            <div class="form-group">
                <label for="txtEmail">Correo electronico</label>
                <input  type="email" 
                        class="form-control bg-transparent text-white" 
                        id="txtEmail" 
                        aria-describedby="emailHelp"
                        v-model="mensaje.email"
                >
            </div>
        </div>
        <div class="col-md-7 mt-4">
            <div class="form-group">
                <label for="txtMensaje">Mensaje</label>
                <textarea   class="form-control bg-transparent text-white" 
                            id="txtMensaje" 
                            rows="4"
                            v-model="mensaje.message"
                ></textarea>
            </div>
            
        </div>
          
      </div>

      <div class="row bg-dark">
          <div class="col text-right">
              <button class="btn btn-warning mb-4" @click.prevent="enviarMensaje()" :disabled="habilitarBoton">
                Enviar comentarios
              </button>
          </div>
      </div>

    </div>
  
</template>

<script>
import axios from 'axios'
export default {
    data() {
        return {
            mensaje:{
                name: '', email:'', message:''
            },
            alert:{
                mensaje:'', show: false, tipo:''
            }      
            
        }
    },
    computed: {
        habilitarBoton() {
            if (this.mensaje.name.length > 0 && this.mensaje.email.length > 0 && this.mensaje.message.length > 0) {
                return false
            } else {
                return true
            }
        }
    },
    methods: {
        enviarMensaje() {
            axios.post('api/contact',this.mensaje)
            .then(response =>{
                console.log(response);
                this.alert.mensaje = 'Gracias por tus comentarios!';
                this.alert.show = true;
                this.alert.tipo = 'alert alert-success'
                this.mensaje.name = ''
                this.mensaje.email = ''
                this.mensaje.message = ''
            })
            .catch(e =>{
                console.log(e.response);
                this.alert.mensaje = e.response.data.message;
                this.alert.show = true;
                this.alert.tipo = 'alert alert-danger'
            })
        }
    },

}
</script>

<style>
    .mi-contact{
        background: #000000;
    }
    .form-control:focus{
        border: 1px solid #FFC700;
        box-sizing: border-box;
        border-radius: 4px;
        
    }
</style>