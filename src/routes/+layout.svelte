<script lang="ts">
	import './layout.css';
	import favicon from '$lib/assets/favicon.svg';
	import * as Sidebar from "$lib/components/ui/sidebar/index.js";
	let { children } = $props();
	import { ModeWatcher, toggleMode } from "mode-watcher";
	import SunIcon from "@lucide/svelte/icons/sun";
  	import MoonIcon from "@lucide/svelte/icons/moon";
	import { Button } from "$lib/components/ui/button/index.js";


</script>

<svelte:head><link rel="icon" href={favicon} /></svelte:head>


<ModeWatcher />

<Sidebar.Provider>
  <Sidebar.Root>
  <Sidebar.Header />
  <Sidebar.Content>
    <Sidebar.Group>
		<Button href="/">Connections</Button>
	</Sidebar.Group>
	<Sidebar.Group>
		<Button href="/templates/">Templates</Button>
	</Sidebar.Group>
	<Sidebar.Group>
		<Button href="/details/">Details</Button>
	</Sidebar.Group>

  </Sidebar.Content>
  <Sidebar.Footer>
	<Button onclick={toggleMode} variant="outline" size="icon">
  <SunIcon class="h-[1.2rem] w-[1.2rem] scale-100 rotate-0 dark:scale-0 dark:-rotate-90" />
  <MoonIcon class="absolute h-[1.2rem] w-[1.2rem] scale-0 rotate-90 dark:scale-100 dark:rotate-0"/>
  <span class="sr-only">Toggle theme</span>
	</Button>
	</Sidebar.Footer>
</Sidebar.Root>
{@render children?.()}
</Sidebar.Provider>