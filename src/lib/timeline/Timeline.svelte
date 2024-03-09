<script>
	import { userData } from '../../data/user';
	import Job from './Job.svelte';
	import Story from './Story.svelte';
	let timeline = userData.timeline;
</script>

<div class="ml-16 mt-5">
	{#each timeline as event}
		{#if event.type === 'story'}
			<Story story={event} />
		{/if}
		{#if event.type === 'job_info'}
			<Job job={event} />
		{/if}
	{/each}
</div>
