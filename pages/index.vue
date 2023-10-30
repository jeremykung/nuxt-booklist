<script setup lang="ts"></script>

<template>
	<div class="home-wrapper">
		<div
			class="absolute w-1/2 h-full flex flex-col justify-center items-center backdrop-blur-md top-0 left-0"
		>
			<h1 class="text-2xl">Reading List</h1>
			<p class="font-thin">Project by Jeremy Kung</p>
		</div>
	</div>
</template>

<style lang="css" scoped>
	* {
		margin: 0;
		padding: 0;
	}
	.home-wrapper {
		background-image: url("../assets/img/blaz-photo-zMRLZh40kms-unsplash.jpg");
		height: 100vh;
		background-size: cover;
		background-position: center;
		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
