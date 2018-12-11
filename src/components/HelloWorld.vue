<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <v-spacer><br><br></v-spacer>
    <h2>Acerca de la distro...</h2>
    
    <ul>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(0)">
          ¿Qué es?
        </v-btn>
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal " @click="verModal(1)">
          ¿Cómo fue construida?
        </v-btn>
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(2)">
          ¿Para qué es?
        </v-btn>
  
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(3)">
          Algunas imágenes
        </v-btn>
  
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(4)">
          ¿Puedo aportar y aprender del código?
  
        </v-btn>
      </li>
      <br>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(5)">
          Licencia
  
        </v-btn>
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="teal" @click="verModal(9)">
          ¿Quién lo realizó?
        </v-btn>
      </li>
    </ul>
    <v-spacer><br><br></v-spacer>
    <h2>Acerca del GLUD</h2>
    <ul>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="light-blue" @click="verModal(6)">
           Grupo GNU Linux UD
        </v-btn>
     
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="light-blue" @click="verModal(7)">
            Universidad Distrital Francisco José de Caldas
        </v-btn>
      
      </li>
      <li>
        <v-btn :disabled="dialog" class="white--text" color="light-blue" @click="verModal(8)">
            Laboratorios Facultad de Ingeniería
        </v-btn>
     
      </li>
  
    </ul>
    
    <v-card>
      <v-card-text>
       ¿Tienes algún comentario o duda? <br> No dudes en escribirnos a: glud@udistrital.edu.co
    </v-card-text>
    </v-card>
  
  
    <v-layout>


      <v-app>
        <v-dialog v-model="dialog" green width="500">
  
  
          <v-card>
            <v-card-title class="headline grey lighten-2" primary-title>
              
            </v-card-title>
  
  
            <v-divider></v-divider>
<v-card>
  <v-card-text>
    {{textos[textoActual]}}
          </v-card-text>
          </v-card>
  
            <v-card-actions>
              <v-spacer></v-spacer>
              <v-btn color="primary" flat @click="dialog = false">
                Cerrar
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-dialog>
      </v-app>
    </v-layout>
  
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        msg: 'Personalización Distribución GNU Linux',
        dialog: false,
        textos: [
          "La distro esta basada en linux mint en su versión 19 (una distribución de GNU/linux basada en Debian y Ubutu, con un núcleo kernel linux) con el entorno de escritorio Cinnamon, “     ”  personaliza mint por medio de un script escrito en shell bash que se encargar de instalar aplicaciones y modificar aspectos del sistema operativo, priorizando la parte visual.",
          "Este proyecto fue creado por iniciativa del GLUD (Grupo GNU Linux de la Universidad Distrital)  y los laboratorios de la facultad de ingeniería de la Universidad Distrital con el objetivo de reemplazar la distribución ubuntu que se usa en los Laboratorios de la facultad de Ingeniería, por una distro hecha por los mismos estudiantes de la Universidad y por ende única.",
          "La distribución se hizo para incentivar el uso de un sistema operativo basado en linux diferente al cotidiano ubuntu, esperando que mas personas usen linux mas frecuentemente y puedan ver las ventajas que tiene un sistema operativo esencialmente libre.",
          " ",
          "El código del Script esta disponible en: https://github.com/GLUD/Pagina_distro",
          "Bajo la Licencia: GNU General Public License v3.0. https://github.com/GLUD/Pagina_distro/blob/master/LICENSE ",
          "https://glud.udistrital.edu.co/",
          "https://www.udistrital.edu.co/",
          "https://labing.udistrital.edu.co/",
          "Brayan Nicolás Mendigaño Madero, Juan Andrés Bayuelo Romero, Diego Alejando Rodriguez Ayala, Edwin Aarón Garcia Pulido, Alejandro Morales, Andrés Mauricio Acosta, Leidy Marcela Aldana"
        ],
        textoActual: 0
      }
    },
    methods: {
      verModal(i) {
        this.textoActual = i;
        this.dialog = true;
      }
    }
  }
</script>

<style scoped>
  h1,
  h2 {
    font-weight: normal;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    display: inline-block;
    margin: 0 10px;
  }
  
  a {
    color: #42b983;
  }
</style>
