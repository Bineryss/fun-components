<script setup lang="ts">
import { PhCheckCircle } from '@phosphor-icons/vue'

defineProps<{
	type: 'success' | 'error' | 'info'
	content: string
}>()
</script>

<template>
	<div class="container">
		<PhCheckCircle class="icon" :size="32" weight="bold" />
		<div class="text-area">
			<h3>{{ content }}</h3>
		</div>
	</div>
</template>

<style lang="css" scoped>
.container {
	margin-inline: 8px;
	position: absolute;
	left: 0;
	bottom: 8px;
	background-color: green;
	border-radius: 4px;
	display: grid;
    grid-template-columns: 64px 0;
	overflow: clip;
    transition: 300ms;

	.icon {
		padding: 16px;
	}

	.text-area {
		display: none;
		border-radius: 4px;
		padding-inline: 8px;
        overflow: clip;

		h3 {
			margin-block: 8px;
            text-align: left;
		}
	}

	&:hover {
		aspect-ratio: unset;
		grid-template-columns: 64px calc(100vw - 80px);
		height: fit-content;

		.text-area {
			display: inline;
            overflow: clip;

            h3 {
                overflow: clip;
            }
		}
	}
}
</style>
