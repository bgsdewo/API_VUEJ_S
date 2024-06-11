<script setup>
import ProductCard from '@/components/ProductCard.vue'
import Pagination from '@/components/Pagination.vue'

import { onBeforeMount,onBeforeUnmount,onBeforeUpdate,onMounted,onUnmounted,onUpdated, ref } from 'vue';

const page = ref(1)

function nextPage() {
	page.value++
}

onBeforeMount(() =>{
	console.log('component will be mounted soon')
	//Lakukan persiapan atau efek samping sebelum mounting 
})

onMounted(() =>{
	console.log('component has been mounted')
	//Lakukan persiapan atau efek samping sebelum mounting 
})

onBeforeUpdate(() =>{
	console.log('component will be updated soon')
	//Lakukan persiapan atau efek samping sebelum mounting 
})

onUpdated(() =>{
	console.log('component has been updated')
	//Lakukan persiapan atau efek samping sebelum mounting 
})

onBeforeUnmount(() =>{
	console.log('component will be unmount soon')
	//Lakukan pembersihan atau persiapan sebelum unmountting
})

onUnmounted(() =>{
	console.log('component has been Unmounted')
	//Lakukan tugas terakhir sebelum dihapus
})
</script>

<template>
	<main>
		{{ page }}
		<button @click="nextPage">Next</button>
		<div class="product-grid">
      <ProductCard />
		</div>
		<div class="pagination">
	<Pagination />
		</div>
	</main>
</template>

<style scoped>
.product-grid {
	display: grid;
	grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
	gap: 20px;
	width: 80%;
	margin: 0 auto;
}
.pagination {
	display: flex;
	justify-content: center;
	align-items: center;
	margin-top: 20px;
}

</style>