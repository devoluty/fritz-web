<script>
	import '../app.css';

	let mode = true;

	function changeMode() {
		mode = !mode;
	}
</script>

<div class="grid grid-cols-8 h-screen">
	<div class="grid col-span-1 bg-[#1e1e1e] text-white content-between font-normal text-sm py-5">
		<div class="grid">
			<a href="/todo" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-regular fa-circle-check mx-3" />To-Do List
			</a>
			<a href="/journal" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-regular fa-pen-to-square mx-3" />Journaling
			</a>
			<a href="/quotes" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-solid fa-quote-right mx-3" />Quotes
			</a>
			<a href="/habits" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-solid fa-apple-whole mx-3" />Habits
			</a>
			<a href="/mission" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-regular fa-eye mx-3" />Mission
			</a>
			<a href="/books" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-solid fa-book mx-3" />Books
			</a>
			<a href="/workout" class="p-3 hover:bg-[#141414] hover:cursor-pointer rounded-lg w-90%">
				<i class="fa-solid fa-dumbbell mx-3" />Workout
			</a>
		</div>
		<div class="grid">
			{#if mode}
				<button class="hover:bg-[#141414] hover:cursor-pointer py-3 m-0" on:click={changeMode}>
					<i class="fa-solid fa-moon" />
				</button>
			{:else}
				<button class="hover:bg-[#141414] hover:cursor-pointer py-3" on:click={changeMode}>
					<i class="fa-solid fa-sun" />
				</button>
			{/if}
		</div>
	</div>
	<slot />
</div>
