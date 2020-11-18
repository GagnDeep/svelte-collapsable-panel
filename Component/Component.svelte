<script>
	export let expanded;

	function open() {
	  expanded = true;
	}

	function close() {
	  expanded = false;
	}

	function toggle() {
	  expanded = !expanded;
	}
</script>

<div class="w-2/3 mx-auto bg-gray-300 my-16">

	<div class="flex flex-col">
		<div class="rounded bg-gray-400 text-gray-600 px-4 text-sm flex items-center">
			<button on:click class="mr-2 inline-block font-bold text-gray-600 hover:text-gray-500">></button>
			<span>label</span>
		</div>
	</div>

	<slot {open} {close} {expanded} {toggle} />

</div>