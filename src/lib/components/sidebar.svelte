<script>
	import Button from "$lib/components/ui/button/button.svelte";
	import {
		HomeIcon,
		MapIcon,
		CameraIcon,
        MessageCircleIcon,
		InfoIcon,
		MoonIcon,
		SunIcon,
		ListIcon,
	} from "svelte-feather-icons";

	import { toggleMode, setMode, resetMode } from "mode-watcher";
	import { goto } from "$app/navigation";
</script>

<div class="max-h-screen border-r-2 border-secondary flex flex-col">
	<div class="flex flex-col w-52 min-h-screen p-3">
		<!-- add a bunch of buttons-->
		<Button
			variant="ghost"
			class="justify-start items-start min-w-full"
			on:click={() => {
				goto("/");
			}}>
			<div class="gap-x-5 flex flex-row text-lg">
				<HomeIcon size="24" />
				Home
			</div>
		</Button>
		<Button
			variant="ghost"
			class="justify-start items-start"
			on:click={() => {
				goto("/app");
			}}>
			<div class="gap-x-5 flex flex-row text-lg">
				<CameraIcon size="24" />
				Scan
			</div>
		</Button>
		<div class="h-full flex flex-col justify-between">
			<div class="w-full"></div>
			<!-- svelte-ignore a11y-no-static-element-interactions -->
			<div
				on:contextmenu|preventDefault={resetMode}
				class="align-bottom object-bottom">
				<p class="sr-only">Right click to reset the theme</p>
				<Button
					variant="ghost"
					on:click={toggleMode}
					class="w-full justify-start items-start">
					<div class="gap-x-5 flex flex-row text-lg">
						<MoonIcon
							size="24"
							class="stroke-accent-100
                        rounded-lg cursor-pointer
                        rotate-90 scale-0 transition-all dark:rotate-0 dark:scale-100
                        " />
						<SunIcon
							size="24"
							class=" absolute
                        rounded-lg cursor-pointer
                        dark:rotate-90 dark:scale-0 transition-all rotate-0 scale-100
                        " />
						Theme
					</div>
				</Button>
			</div>
		</div>
	</div>
</div>
