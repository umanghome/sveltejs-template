<div>
	<input type="checkbox" id="round" bind:checked="round" />
	<label for="round">Round</label>
</div>

<WithoutSpread
	{classes}
	{reverse}
>
	Without Spread
</WithoutSpread>

<WithSpread
	{reverse}
	{classes}
	attributes={{
		'aria-label': 'With Spread'
	}}
>
	With Spread
</WithSpread>

<script>

export default {
	components: {
		WithoutSpread: './WithoutSpread.svelte',
		WithSpread: './WithSpread.svelte',
	},

	data: () => ({
		reverse: true,
	}),

	computed: {
		classes: ({ round }) => {
			const allClasses = [];

			if (round) {
				allClasses.push('round');
			}

			return allClasses;
		}
	},
}

</script>

<style>
	label, input {
		display: inline-block;
		vertical-align: top;
	}
</style>