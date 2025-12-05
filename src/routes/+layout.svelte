<script lang="ts">
  import "../app.css";
  import favicon from "$lib/assets/favicon.svg";
  import Header from "../components/Header.svelte";
  import Footer from "../components/Footer.svelte";
  import Particles from "../components/Particles.svelte";

  let { children } = $props();
  let y: number;
  let innerHeight: number = 0;
  let innerWidth: number = 0;

  function goTop() {
	document.body.scrollIntoView()
  }

</script>

<svelte:head>
  <link rel="icon" href={favicon} />
</svelte:head>

<div
  class="relative flex flex-col max-w-[1400px] mx-auto w-full text-sm sm:text-base min-h-screen use:addSparticles"
>
	<div class={"fixed bottom-0 w-full duration-200 flex p-10 z=[10]" +
		(y > 0 ? 'opacity-full pointer-events-auto':'pointer-events-none opacity-0')
		}>
		<button 
      onclick={goTop} 
      class="ml-auto rounded-full aspect-square bg-slate-900 text-teal-400 px-3 sm:px-4 hover:bg-slate-800 cursor-pointer flex items-center justify-center"
      >
      <i class="fa-solid fa-arrow-up"></i>
    </button>
	</div>
	<Header y={y}/>
	{@render children()}
	<Footer />
  <Particles className="absolute inset-0" refresh={true} />
</div>

<svelte:window bind:scrollY={y} bind:innerHeight bind:innerWidth />