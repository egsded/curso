<template>
	<div>
		<b-list-group>
  <b-list-group-item v-for="(item, index) of mugrero" :key="item.id" @click="aumentar(index)"
   class="d-flex justify-content-between align-items-center">
    {{index}} - {{item.nombre}}
    <b-badge variant="primary" pill>{{item.cantidad}}</b-badge>
  </b-list-group-item>
</b-list-group>
<b-button block variant="danger" @click="reiniciar">Reiniciar</b-button>
	</div>
</template>
<script>
import {mapState, mapMutations} from 'vuex';
	export default{
		name: 'Lista',
		computed:{
			...mapState(['frutas']),
			mugrero(){
				return this.frutas.sort( (a, b) => b.cantidad - a.cantidad);
			}
		},
		methods:{
			...mapMutations(['aumentar', 'reiniciar'])
		}
	}
</script>
