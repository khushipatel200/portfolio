<script>
	import ArtCell from '../atoms/Artwork.svelte';
</script>

<div class="grid-container">
	<div class="grid">
		<ArtCell art="art1" tall />
		<ArtCell art="art2" />
		<ArtCell art="art3" tall />
		<ArtCell art="art4" />
		<ArtCell art="art5" tall />
		<ArtCell art="art6" tall />
		<ArtCell
			art="art7"
			tall
			shrink
			commission
			bottomText="Commissioned by Kevin T#0001 · Do not use"
		/>
		<ArtCell art="art8" tall />
		<ArtCell art="art9" />
		<ArtCell art="art10" />
	</div>
</div>

<style lang="scss">
	@import '../../styles/mixins.scss';

	.grid {
		gap: 0.8rem;
		grid-auto-rows: 230px;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
		width: min(90%, 72rem);

		@media screen and (max-width: 600px) {
			grid-auto-rows: 125px;
		}

		@media screen and (max-width: 868px) {
			width: min(100%, 75rem);
			gap: 0.2rem;
			grid-template-columns: 1fr 1fr 1fr;
		}

		&:before {
			@include outlineText($content: '&&', $translateX: -40%, $translateY: -160%);

			@media screen and (max-width: 868px) {
				@include outlineText($content: '&&', $translateX: -25%, $translateY: -95%);
			}
		}
	}

	.grid-container {
		display: flex;
		justify-content: center;
		margin-bottom: 4rem;
	}
</style>
