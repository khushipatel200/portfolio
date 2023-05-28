<script>
	import Tooltip from '../atoms/Tooltip.svelte';
	import Socials from './Socials.svelte';
</script>

<hr />
<footer class="wrapper">
	<Socials />
	<h6>
		Made with pain. &#60;3
		
	</h6>
</footer>

<style lang="scss">
	hr {
		background-color: var(--neutral-one);
		height: 1px;
		border: 0;
		width: 100%;
		margin-bottom: 2rem;

		@media screen and (max-width: 768px) {
			margin-bottom: 1.5rem;
		}
	}

	footer {
		padding-bottom: 2.4rem;
		display: flex;
		justify-content: space-between;
		align-items: center;

		@media screen and (max-width: 768px) {
			flex-direction: column;
		}
	}

	h6 {
		text-align: center;
		line-height: 2.5rem;
		margin-top: 0;
	}

</style>
