<script>
import DataBase from '../assets/db.json'

export default {
	data() {
		return {
			products: DataBase.products
		}
	},
	components: {
		DataBase
	},
	methods: {
		
	},
	props: [
		// frontImage
		],
}
</script>

<template>
	<section class="page-content">
		<div class="section products">
			<div class="container">
				<ul class="row">
					<li v-for="product in products" :key="product.id" class="col-12 col-md-6 col-lg-4">
						<!-- <img :img="product.frontImage" alt=""> -->
						<!-- {{ product.brand }} -->
						<div class="card product">
							<div class="card__header">
								<!-- stampare le immagini correttamente -->
								<img class="product__thumb" src="/img/1.webp" alt="" />
								<img class="product__thumb thumb--hover" src="/img/1b.webp" alt="" />
								<span v-if="product.isInFavorites == true" class="btn-heart">
									&hearts;
								</span>
								<ul class="badges">
									<li v-for="badge in product.badges" :key="product.id" :class="badge.type == 'tag' ? 'badge badge--sostenibility':'badge badge--discount'">
										{{ badge.value }}
									</li>
								</ul>
							</div>
							<div class="card__body">
								<strong class="product__brand"> {{ product.brand }}</strong>
								<h3 class="product__title"> {{ product.name }}</h3>
								<div class="product__price">
									<span>{{ product.price }}&euro;</span>
								</div>
							</div>
						</div>
					</li>
					<!-- <div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
								<img class="product__thumb thumb--hover" src="/img/1b.webp" alt="" />
								<span class="btn-heart">&hearts;</span>
								<ul class="badges">
									<li class="badge badge--discount">-50%</li>
									<li class="badge badge--sostenibility">Sostenibilità</li>
								</ul>
							</div>
							<div class="card__body">
								<strong class="product__brand">Levi's</strong>
								<h3 class="product__title">Relaxed fit tee unisex</h3>
								<div class="product__price">
									<span>14,99 &euro;</span>
								</div>
							</div>
						</div>
					</div> -->
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