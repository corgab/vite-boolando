<script>
import DataBase from '/db.json'
import CardProduct from './CardProduct.vue'
import { store } from '../store.js'

export default {
	data() {
		return {
			store
		}
	},
	components: {
		CardProduct
	},
	methods: {
		
	},

}
</script>

<template>
	<section class="page-content">
		<div class="section products">
			<div class="container">
				<ul class="row">
					<CardProduct v-for="product in store.data" :key="product.id" :product="product"/>
				</ul>
			</div>
		</div>
	</section>
</template>

<style lang="scss" scoped>
.card__header img {
	display: block;
}

.card.product .card__header {
	position: relative;
}

.badges {
	display: flex;
	flex-wrap: wrap;
	gap: 8px;
	position: absolute;
	left: 0;
	bottom: 20px;
}

.badge--discount {
	background-color: red;
}

.badge--sostenibility {
	background-color: green;
}

.product__thumb {
	aspect-ratio: 1/1;
	width: 100%;
	object-fit: cover;
	object-position: center center;

	&.thumb--hover {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		opacity: 0;
		transition: opacity 300ms ease-in-out;
	}
}

.card:hover .product__thumb.thumb--hover {
	opacity: 1;
}

.product__price {

	:first-child {
		color: red;
		font-weight: 700;
	}
}

.product__price :nth-child(2) {
	color: #555;
}
</style>