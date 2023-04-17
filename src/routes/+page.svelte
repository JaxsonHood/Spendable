<script>
	import NumericUpDown from '../components/NumericUpDown.svelte';
</script>

<div class="h-screen w-full relative overflow-hidden text-gray-300 bg-gray-950 p-4">
	<div class="flex row w-full">
		<div class="text-3xl font-bold">Spendable</div>
	</div>

	<div class="w-full h-1 rounded-sm bg-gray-900 my-3" />

	<div class="flex row w-full mb-2 space-x-2">
		<div>
			<label for="price" class="block text-sm font-medium leading-6 text-gray-600"
				>Hourly Wage</label
			>
			<div class="relative mt-0.5 rounded-md shadow-sm">
				<div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-3">
					<span class="text-gray-500">$</span>
				</div>
				<input
					type="text"
					name="wage"
					id="wage"
					class="block w-[150px] rounded-lg border-0 py-1.5 pl-7 pr-10 placeholder:text-gray-700 text-gray-400 sm:leading-6 focus:outline-none focus:ring-2 focus:ring-gray-700 bg-gray-900"
					placeholder="0.00"
				/>
			</div>
		</div>
		<div>
			<label for="price" class="block text-sm font-medium leading-6 text-gray-600"
				>Hours Per Week</label
			>
			<NumericUpDown />
		</div>

        <div>
			<label for="price" class="block text-sm font-medium leading-6 text-gray-600"
				>Income Tax %</label
			>
			<div class="relative mt-0.5 rounded-md shadow-sm">
				
				<input
					type="text"
					name="tax"
					id="tax"
					class="block w-[105px] rounded-lg border-0 py-1.5 pl-7 pr-10 placeholder:text-gray-700 text-gray-400 sm:leading-6 focus:outline-none focus:ring-2 focus:ring-gray-700 bg-gray-900"
					placeholder="0.0"
				/>
                <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-6">
					<span class="text-gray-500">%</span>
				</div>
			</div>
		</div>
		<div>
			<label for="price" class="block text-sm font-medium leading-6 text-gray-600"
				>Weekly Save %</label
			>
			<div class="relative mt-0.5 rounded-md shadow-sm">
				
				<input
					type="text"
					name="tax"
					id="tax"
					class="block w-[105px] rounded-lg border-0 py-1.5 pl-7 pr-10 placeholder:text-gray-700 text-gray-400 sm:leading-6 focus:outline-none focus:ring-2 focus:ring-gray-700 bg-gray-900"
					placeholder="0.0"
				/>
                <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-6">
					<span class="text-gray-500">%</span>
				</div>
			</div>
		</div>
	</div>
</div>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.gray.950);
	}
</style>
