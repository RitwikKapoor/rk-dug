<script lang="ts">
	export let story: any;
	import Card from './Card.svelte';
	import sym_story from '/sym_story.svg';
</script>

<div class="flex items-center">
	<div class="relative flex h-[274px] w-40 items-center border-r-4 border-dotted py-4">
		<div class="ml-auto py-4">
			<p
				class="ml-auto mr-5 h-[15px] w-[56px] text-right text-xs font-normal leading-[14.52px] text-[#7A9299]"
			>
				{story.date}
			</p>
		</div>

		<div class="absolute -right-2.5">
			<img src={sym_story} alt="circle" />
		</div>
	</div>

	<div class="ml-5 flex gap-9 px-6 py-2">
		{#each story.content as { title, thumbnail }}
			<Card {title} {thumbnail} />
		{/each}
	</div>
</div>
