<template>
  <div id="app" class="container">
    <Cabecera></Cabecera>
    <Lista></Lista>
  </div>
</template>

<script>
import Cabecera from './components/Cabecera.vue'
import Lista from './components/Lista.vue'
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)

export default {
  name: 'app',
  components: {
    Cabecera,
    Lista
  }
}

</script>
