<script lang="ts">
	let links = [
		{
			id: `twitter`,
			text: `@me`,
			url: `https://twitter.com/cdercer`
		},
		{
			id: `suaveseals`,
			text: `@suaveseals`,
			url: `https://twitter.com/SuaveSeals`
		}
	];
</script>

<div class="container  parent--  grow--  col--  col-centre--  landing">
	<div class="container  grow--  stretch--  col--  col-centre--  col-middle--">
		<img src="./images/werd.png" alt="" class="landing-text-image" />
	</div>

	<div class="container  parent--  stretch--  row--  row-centre--  row-bottom--">
		<img src="./images/cat.png" alt="" class="landing-cat-image" />
		<div class="container  parent-=-  grow--  row--  row-right--  landing-links">
			{#each links as link}
				<a href={link.url} target="_blank" class="landing-link">
					{link.text}
				</a>
			{/each}
		</div>
	</div>
</div>

<style lang="scss">
	@import '../assets/scss/all.scss';

	.landing {
		width: calc(100% - $wrapper-gutter * 2);
		max-width: 1000px;
		font-family: 'IBM Plex Mono';
	}

	.landing-text-image {
		@include pixel-art;
		width: 15em;

		@media (min-width: $bp-md) {
			width: 33em;
		}
	}

	.landing-cat-image {
		@include pixel-art;
		width: 10em;

		@media (min-width: $bp-md) {
			width: 20em;
		}
	}

	.landing-links {
		padding: 1.2em;

		@media (min-width: $bp-md) {
			padding: 2.4em;
		}
	}

	.landing-link {
		color: #8b93af;
		font-size: 0.9em;
		@include swish;

		@media (min-width: $bp-md) {
			font-size: 1.8em;
		}

		&:hover {
			color: #4a5462;
			text-decoration: underline;
		}

		&:not(:first-of-type) {
			margin-left: 0.6em;
		}
	}
</style>
