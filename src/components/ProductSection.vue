<script>
export default {
	data() {
		return {

		}
	}
}
</script>

<template>
	<section class="page-content">
		<div class="section products">
			<div class="container">
				<div class="row">
					<div class="col-12 col-md-6 col-lg-4">
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
					</div>
					<div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
								<span class="btn-heart">&hearts;</span>
								<ul class="badges">
									<li class="badge badge--discount">-50%</li>
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
					</div>
					<div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
								<ul class="badges">
									<li class="badge badge--sostenibility">Sostenibilità</li>
								</ul>
							</div>
							<div class="card__body">
								<strong class="product__brand">Levi's</strong>
								<h3 class="product__title">Relaxed fit tee unisex</h3>
								<div class="product__price">
									<span>14,99 &euro;</span>
									<del>29,99 &euro;</del>
								</div>
							</div>
						</div>
					</div>
					<div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
							</div>
							<div class="card__body">
								<strong class="product__brand">Levi's</strong>
								<h3 class="product__title">Relaxed fit tee unisex</h3>
								<div class="product__price">
									<span>14,99 &euro;</span>
									<span>29,99 &euro;</span>
								</div>
							</div>
						</div>
					</div>
					<div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
							</div>
							<div class="card__body">
								<strong class="product__brand">Levi's</strong>
								<h3 class="product__title">Relaxed fit tee unisex</h3>
								<div class="product__price">
									<span>14,99 &euro;</span>
									<span>29,99 &euro;</span>
								</div>
							</div>
						</div>
					</div>
					<div class="col-12 col-md-6 col-lg-4">
						<div class="card product">
							<div class="card__header">
								<img class="product__thumb" src="/img/1.webp" alt="" />
							</div>
							<div class="card__body">
								<strong class="product__brand">Levi's</strong>
								<h3 class="product__title">Relaxed fit tee unisex</h3>
								<div class="product__price">
									<span>14,99 &euro;</span>
									<span>29,99 &euro;</span>
								</div>
							</div>
						</div>
					</div>
				</div>
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