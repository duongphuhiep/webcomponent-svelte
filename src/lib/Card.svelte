<svelte:options tag="my-card" />

<script>
	// component props
	// Camel case not supported for props, see drawback section.
	export let card_title, card_desc, card_img;
</script>

<main>
	<div class="card-container" part="card-container">
		<div class="card">
			<img src={card_img} alt="My product" part="card-img" />
			<div class="card-body" part="card-body">
				<div class="row">
					<div class="card-title" part="card-title">
						<h2>{card_title}</h2>
					</div>
				</div>
				<p part="card-desc">
					{card_desc}
				</p>
				<button part="button">Do Something</button>
			</div>
		</div>
	</div>
</main>

<style lang="scss">
	.card {
		max-width: 350px;
		border-radius: 5px;
		box-shadow: 0 4px 6px 0 #00000033;
		padding: 0 0 10px 0;

		img {
			width: 100%;
			height: auto;
		}
	}

	.card-body {
		padding: 5px 10px;
		p {
			color: #da2121;
			margin-bottom: 20px;
			font-size: 14px;
		}
	}
</style>
