<script>
import { store } from '../store.js'
export default {
    props: {
        product: Object
    },

    data() {
        return {
            store
        }
    }
}
</script>

<template>
    <li class="col-12 col-md-6 col-lg-4">
        <div class="card product">
            <div class="card__header">
                <img class="product__thumb" :src="'/img/' + product.frontImage" alt="" />
                <img class="product__thumb thumb--hover" :src="'../public/img/' + product.backImage" alt="" />
                <span v-if="product.isInFavorites == true" class="btn-heart">
                    &hearts;
                </span>
                <ul class="badges">
                    <li v-for="badge in product.badges" :key="product.id"
                        :class="badge.type == 'tag' ? 'badge--sostenibility' : 'badge--discount'" class="badge">
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