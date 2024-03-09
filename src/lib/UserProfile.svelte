<script>
	import { userData } from '../data/user.js';
	import icon_redirect from '/icon_redirect.svg';
	import icon_three_dots from '/icon_three_dots.svg';
	let isFollowed = false;

	function toggleFollow() {
		isFollowed = !isFollowed;
	}
</script>

<div class="ml-40 flex w-[80%] flex-row gap-x-14">
	<div class="flex flex-shrink-0 flex-col items-center gap-4">
		<img
			src={userData.profile_img}
			alt="Profile Pic"
			class="h-[120px] w-[120px] rounded-[120px] border-[5px] border-[#EAEFF5]"
		/>
		<p class="max-h-[56px] max-w-[156px] text-center text-2xl/7 font-bold text-[#4B5C6D]">
			{userData.name}
		</p>
	</div>
	<div class="flex flex-col gap-8">
		<div class="flex flex-row items-center justify-between gap-20">
			<p class="w-[71%] gap-2 pr-2 text-sm/6 font-normal text-[#141618]">{userData.summary}</p>
			<div class="flex flex-col items-end gap-1">
				<img class="w-10 rounded-full" alt={userData.company} src={userData.company_img} />
				<p class="text-right text-base font-bold leading-[19.36px]">{userData.company}</p>
				<p class="text-right text-xs font-normal leading-[14.52px] text-[#7A9299]">
					{userData.position}
				</p>
			</div>
		</div>
		<div class="flex flex-row items-center justify-between gap-4">
			<button
				class={`flex h-[36px] w-[91px] items-center justify-center rounded-[4px] border-[0.5px] px-[16px] text-xs font-normal leading-[14.52px] text-[#4D4D4D]  transition-all duration-150 hover:border-blue-800 hover:bg-[#0066FF] hover:text-white hover:shadow-blue_shadow ${isFollowed ? 'shadow-btn_shadow2' : 'shadow-btn_shadow '}`}
				on:click={toggleFollow}
			>
				<div class="gap-[8px] p-[8px]">
					{#if isFollowed}
						Followed
					{:else}
						Follow
					{/if}
				</div>
			</button>
			<div class="flex items-center gap-4">
				<a class="flex items-center gap-2 text-sm font-normal text-[#4D4D4D]" href="/">
					My website
					<img alt="website" src={icon_redirect} />
				</a>
				<img alt="three dots" src={icon_three_dots} class="cursor-pointer" />
			</div>
		</div>
	</div>
</div>
