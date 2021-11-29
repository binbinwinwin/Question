<template>
    <div id="container">
    <cardtest title="123"></cardtest>
	</div>
</template>

<script>
import Vue from 'vue/dist/vue.esm.js';

Vue.component('cardtest',{
	props: ['title'],
	template:`
		<div>456
		</div>
	`,
});

export default {
	data(){
		return{
		}
	},
}

</script>