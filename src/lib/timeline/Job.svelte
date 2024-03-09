<script lang="ts">
	export let job: any;
	import sym_job from '/sym_job.svg';
	import arrow from '/arrow.svg';
</script>

<div class="flex items-center">
	<div class="relative flex h-40 w-40 items-center border-r-4 border-dotted py-4">
		<div class="flex flex-col gap-y-[8px]">
			<img class="ml-auto h-12 w-12 rounded-[90px]" src={job.company_img} alt="company" />
			<h3 class="text-right text-base font-bold leading-[19.36px] text-[#141618]">{job.company}</h3>
			<p class="h-[15px] w-[134px] text-right text-xs font-normal leading-[14.52px] text-[#7A9299]">
				{job.location}
			</p>
			<p class="h-[30px] w-[56x] text-right text-xs font-normal leading-[14.52px] text-[#7A9299]">
				Joined <br />
				{job.date}
			</p>
		</div>

		<div class="absolute -right-4">
			<img src={sym_job} alt="circle" />
		</div>

		<div class="absolute -right-2.5 top-0">
			<img class="w-4" src={arrow} alt="arrow" />
		</div>
	</div>

	<div class="ml-5 px-6 py-2">
		<div class="w-full max-w-2xl bg-white px-5 py-4 shadow-job_shadow">
			<h2 class="text-xl/8 font-bold text-[#141618]">{job.title}</h2>
			<p class="h-[15px] w-[103px] text-xs leading-[14.52px] text-[#7A9299]">{job.job_style}</p>
		</div>
	</div>
</div>
