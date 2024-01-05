<script setup lang="ts">
	import TheHeader from './components/TheHeader.vue'
</script>

<template>
	<the-header />

	<the-footer />
</template>

<style>
	body {
		margin: 0 auto;
		font-family: 'Roboto', sans-serif;
		width: 1366px;
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
		padding: 0 98px;
	}
</style>