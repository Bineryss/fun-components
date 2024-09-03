<script setup lang="ts">
import SmartToast from './components/SmartToast.vue'

const text = 'lorem ipsum dolorem isage regrabo cano lorem lorem ipsum dolorem isage regrabo cano lorem ipsum dolorem isage regrabo cano ipsum dolorem isage regrabo cano'
</script>

<template>
	<h1>hello</h1>
	<SmartToast class="top" type="success" :content="text" />
	<SmartToast type="success" :content="text" />
</template>

<style scoped>
.top {
	bottom: 200px;
}
</style>
