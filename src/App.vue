<script setup lang="ts">
	import TheHeader from './components/TheHeader.vue'
</script>

<template>
	<div class="wrapper">
		<the-header />

		<the-footer />
	</div>
</template>

<style>
	body {
		margin: 0;
		font-family: 'Roboto', sans-serif;
	}

	.wrapper {
		width: 1366px;
		margin: 0 auto;
	}

	:root {
		--link-color: #122659;
		--color-red: #ed1c21;
	}

	a {
		display: block;
		text-decoration: none;
		color: var(--link-color);
	}

	ul {
		padding: 0;
		list-style: none;
	}

	.container {
		margin-right: auto;
		margin-left: auto;
	}
</style>