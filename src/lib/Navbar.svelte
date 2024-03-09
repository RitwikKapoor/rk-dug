<script>
	import main_logo from '/main_logo.svg';
	import icon_home from '/icon_home.svg';
	import icon_explore from '/icon_explore.svg';
	import icon_learn from '/icon_learn.svg';
	import icon_down from '/icon_down.svg';
	import icon_plus from '/icon_plus.svg';
	import avatar from '/avatar.jpeg';
	import Button from '$lib/components/ui/button/button.svelte';
</script>

<nav
	class="fixed z-50 flex min-h-[73px] w-full max-w-[1424px] justify-between border-b-2 border-dotted bg-white pt-[10px]"
>
	<img src={main_logo} alt="duggup-logo" class="cursor-pointer" />
	<div class="flex flex-row items-center gap-x-10">
		<div class="flex cursor-pointer items-center">
			<div class="flex items-center px-[16px]">
				<div class="px-[10px]">
					<img src={icon_home} alt="home" />
				</div>
				<p>Home</p>
			</div>

			<div class="flex cursor-pointer items-center px-[16px]">
				<div class="px-[10px]">
					<img src={icon_explore} alt="explore" />
				</div>
				<p>Explore</p>
			</div>

			<div class="flex cursor-pointer items-center px-[16px]">
				<div class="px-[10px]">
					<img src={icon_learn} alt="learn" />
				</div>
				<p>Learn</p>
			</div>
		</div>
		<Button variant="custom" size="custom_size">
			<img src={icon_plus} alt="plus" class="p-[4px]" />
			<div class="p-[8px]">
				<p class="text-left text-sm font-normal">Post</p>
			</div>
		</Button>
		<div class="mr-10 flex items-center gap-x-3 px-4">
			<img
				class="w-12 rounded-[1000px] border-[0.5px] border-[#4D4D4D]"
				src={avatar}
				alt="profile"
			/>
			<p class="font-medium">Krishna Kiran</p>
			<img class="w-2" src={icon_down} alt="profile-menu" />
		</div>
	</div>
</nav>
