<script>
    let value = 0;

	function increment() {
		value += 1;
	}
    function decrement() {
		if ( value > 0 )
            value -= 1;
	}
</script>

<div class="custom-number-input h-9 w-32">
	<div class="flex flex-row h-9 w-full rounded-xl relative bg-transparent mt-0.5">
		<button
			data-action="decrement"
            on:click={decrement}
			class=" bg-gray-900 text-gray-600 hover:text-gray-300 hover:bg-gray-800 h-full w-20 rounded-l-lg cursor-pointer outline-none"
		>
			<span class="m-auto text-2xl font-thin">−</span>
		</button>

		<input
			type="number"
			class="outline-none focus:outline-none text-center w-full bg-gray-900 font-semibold text-md hover:text-gray-200 focus:text-white md:text-basecursor-default flex items-center text-gray-300"
			name="custom-input-number"
			bind:value={value}
		/>

		<button
			data-action="increment"
            on:click={increment}
			class="bg-gray-900 text-gray-600 hover:text-gray-300 hover:bg-gray-800 h-full w-20 rounded-r-lg cursor-pointer"
		>
			<span class="m-auto text-2xl font-thin">+</span>
		</button>
	</div>
</div>

<style>
	input[type='number']::-webkit-inner-spin-button,
	input[type='number']::-webkit-outer-spin-button {
		-webkit-appearance: none;
		margin: 0;
	}

	.custom-number-input input:focus {
		outline: none !important;
	}

	.custom-number-input button:focus {
		outline: none !important;
	}
</style>
