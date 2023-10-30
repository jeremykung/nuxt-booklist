<!-- import type { dropdown } from '@nuxt/ui/dist/runtime/ui.config'; import type {
dropdown } from '@nuxt/ui/dist/runtime/ui.config'; import type { ColorModeButton
} from '#ui-colors/components'; -->
<script setup>
	const isOpen = ref(false)
</script>

<template>
	<div>
		<!-- CLOSED -->
		<div
			class="py-4 pr-6 flex justify-end items-center gap-4 absolute w-full"
		>
			<ColorModeButton />
			<UIcon
				name="i-heroicons-bars-3"
				class="p-3 hover:cursor-pointer"
				@click="isOpen = true"
			/>
		</div>

		<!-- OPEN -->
		<USlideover v-model="isOpen">
			<UCard
				class="flex flex-col flex-1"
				:ui="{
					body: { base: 'flex-1' },
					ring: '',
					divide: 'divide-y divide-gray-100 dark:divide-gray-800',
				}"
			>
				<template #header>
					<!-- Content -->
					<nav class="p-4">
						<NuxtLink to="/">Reading List</NuxtLink>
					</nav>
				</template>

				<!-- Content -->
				<nav class="mx-auto p-4 gap-4 flex flex-col justify-center">
					<NuxtLink to="/">Home</NuxtLink>
					<NuxtLink to="/Seach">Search</NuxtLink>
				</nav>

				<template #footer>
					<!-- Content -->
				</template>
			</UCard>
		</USlideover>
	</div>
</template>
