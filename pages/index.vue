<template>
	<div>
		<div class="container">
			<h1>Sotware Developer</h1>
		</div>
		<div class="container">
			<h1>
				<nuxt-link to="/projects" class="button--green"
					>projects</nuxt-link
				>
			</h1>
		</div>
		<div class="container">
			<h1>
				<nuxt-link to="/about" class="button--green">about</nuxt-link>
			</h1>
		</div>
		<div class="container">
			<logo></logo>
		</div>
	</div>
</template>

<script>
import Logo from '../components/Logo';
export default {
	components: {
		Logo,
	},
};
</script>

<style>
.title {
	font-family: 'Quicksand', 'Source Sans Pro', -apple-system,
		BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial,
		sans-serif;
	display: block;
	font-weight: 300;
	font-size: 100px;
	color: #35495e;
	letter-spacing: 1px;
}

.subtitle {
	font-weight: 300;
	font-size: 42px;
	color: #526488;
	word-spacing: 5px;
	padding-bottom: 15px;
}

.links {
	padding-top: 15px;
}
</style>
