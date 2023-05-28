<script>
	import RichPresence from '../molecules/RichPresence.svelte';
	import Tooltip from '../atoms/Tooltip.svelte';

	// i didnt write this idk
	let getAge = () => {
		let birthDate = new Date('2003/02/10');
		const ageMs = Date.now() - birthDate.getTime();
		const preciseAge = (ageMs / 31536000000).toFixed(10);
		return preciseAge;
	};

	let age = getAge();
	setInterval(() => {
		age = getAge();
	}, 1000);
</script>

<section id="about" class="wrapper">
	<div>
		<!-- <RichPresence /> -->
	</div>
	<div class="text">
		<h2>bio</h2>
		<p>
			My name is <span>Bijal</span> patel, I'm currently <Tooltip tip={age}
			><span>{Math.floor(Number(age))}</span></Tooltip
		>  years old. I was born in Surat, Gujarat. I possess a passion for graphic design and illustration, and I have developed considerable skills in these areas. As a creative individual, I am constantly seeking new challenges in my life that can help me improve both my skills and myself as a whole. I believe in utilizing my knowledge and abilities to the fullest extent, and I am always prepared to give my best effort in any task or project that comes my way. I am eager to take on exciting opportunities that allow me to showcase my talents and contribute to the creative industry.</p>
	</div>
</section>

<style lang="scss">
	@import '../../styles/mixins.scss';

	section {
		margin-bottom: 6rem;
		// display: grid;
		// gap: 4.5rem;
		// grid-template-columns: 1fr 1fr;
		align-items: center;
	}

	.text {
		position: relative;
		line-height: 1.75rem;
	}

	span {
		font-weight: 400;
		font-family: var(--font-two);
		font-size: 0.9rem;
		background-color: var(--neutral-one);
		border-radius: 7px;
		color: var(--yellow);
		padding: 0.2rem 0.5rem 0.2rem;
		width: fit-content;
	}

	a {
		text-decoration: none;
	}

	.text::before {
		@include outlineText($content: 'BIJAL', $translateX: 97%, $translateY: -5%, $fontSize: 300px, $opacity: 0.22);
	}

	h2 {
		display: none;
		margin-top: 1rem;
	}

	@media (max-width: 868px) {
		section {
			display: flex;
			flex-direction: column;
			align-items: normal;
		}

		h2 {
			display: block;
			margin-bottom: 1rem;
		}
	}
</style>
