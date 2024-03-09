<script>
	export let title = '';
	export let thumbnail = '';
</script>

<div class="w-[344px] overflow-hidden rounded-xl border-[0.5px] border-[#D0D5DD]">
	<img class="h-36 w-full object-cover" src={thumbnail} alt="story card" />
	<div class="p-6">
		<p class="text-sm font-normal leading-[21px]">{title}</p>
	</div>
</div>
