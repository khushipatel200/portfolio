<script>
	import Social from '../atoms/Social.svelte';
	import { user } from '../../util/discord';
</script>

<div class="socials-container">
	<Social icon="email" tip="khushi4379@gmail.com" link="mailto:khushi4379@gmail.com" />
	<Social icon="behance" tip="khushi Patel" link="https://www.behance.net/khushipatel30?tracking_source=search_users|khushi%20patel" />
	<!-- <Social icon="discord" tip={user.fullName()} link={``} /> -->
	<!-- <Social icon="kofi" tip="@affan" link="https://ko-fi.com/affan" /> -->
</div>

<style>
	.socials-container {
		display: flex;
		gap: 0.75rem;
	}
</style>
