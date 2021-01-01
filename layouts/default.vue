<template>
	<div>
		<div class="navbar-background">
			<div class="bootstrap">
				<nav class="navbar navbar-expand-lg navbar-light bg-black">
					<div class="container">
						<nuxt-link to="/" class="button--grey">home</nuxt-link>
						<nuxt-link to="/projects" class="button--green"
							>projects</nuxt-link
						>
						<nuxt-link to="/about" class="button--green"
							>about</nuxt-link
						>
					</div>
				</nav>
			</div>
		</div>
		<Nuxt />
	</div>
</template>

<style>
html {
	font-family: 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
		'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
	font-size: 16px;
	word-spacing: 1px;
	-ms-text-size-adjust: 100%;
	-webkit-text-size-adjust: 100%;
	-moz-osx-font-smoothing: grayscale;
	-webkit-font-smoothing: antialiased;
	box-sizing: border-box;
}
.container {
	margin: 0 auto;
	margin-top: 1rem;
	min-height: 10vh;
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
}
*,
*::before,
*::after {
	box-sizing: border-box;
	margin: 0;
}
.bootstrap {
	margin: auto;
	width: 400px;
	background-color: black;
}
.navbar-background {
	background-color: black;
}

.button--green {
	display: inline-block;
	border-radius: 4px;
	border: 1px solid #3b8070;
	color: #3b8070;
	text-decoration: none;
	padding: 10px 30px;
}

.button--green:hover {
	color: #fff;
	background-color: #3b8070;
}

.button--grey {
	display: inline-block;
	border-radius: 4px;
	border: 1px solid #35495e;
	color: #35495e;
	text-decoration: none;
	padding: 10px 30px;
	margin-left: 15px;
}

.button--grey:hover {
	color: #fff;
	background-color: #35495e;
}
</style>
