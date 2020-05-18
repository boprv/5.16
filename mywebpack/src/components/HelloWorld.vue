<template>
	<div class="hello">
		<input type="text" v-model="msg" @keydown.enter="enter" />
		<p class="red">{{toupper}}</p>
		<child cmsg="阿西吧" @change="getval"></child>
	</div>
</template>

<script>
	import child from './child'
	export default {
		name: 'HelloWorld',
		components: {
			child
		},
		data() {
			return {
				msg: 'asd'
			}
		},
		computed: {
			toupper() {
				return this.msg.toUpperCase()
			}
		},
		methods: {
			enter() {
				alert(this.msg)
			},
			getval(val){
				console.log(val)
			}
		}
	}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
	.red {
		color: red;
	}
</style>