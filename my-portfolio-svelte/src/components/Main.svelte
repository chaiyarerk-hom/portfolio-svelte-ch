<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "E-Commerce Store", icon: "fa-solid fa-cart-shopping", href:"https://ecom-svelte-port-ch.vercel.app/" },
    { name: "Biotech Store", icon: "fa-solid fa-flask", href:"https://ecom-nextjs-app-ch.vercel.app/" },
  ];

  let benefits = [
    {name: 'an active-learning developer', description: 'Constantly exploring new technologies and programming approaches to stay ahead. Able to adapt quickly and creatively solve unfamiliar challenges.'},
    {name: 'a chemical and bioprocess engineer', description: 'Applies deep scientific knowledge to develop innovative, domain-specific solutions. Bridges the gap between complex biological problems and practical software tools.'},
    {name: 'an excellent communicator', description: 'Explains technical and scientific concepts clearly to diverse audiences. Enhances collaboration and efficiency across teams and projects.'},
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-teal-400">Chaiyarerk</span> Ant
        <br />Newbie
        <span class="poppins text-teal-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violot-400">favorite tech</span> includes TypeScript
        (NEXT.JS or SvelteKit), TailwindCSS, Node.js + Express.js, PostgreSQL and
        Flutter with Firebase for cross-platform app development
      </p>
      <a
        href="https://www.linkedin.com/in/chaiyarerk-homsirikamol-a83b83203/"
        target="_blank"
        class="blueShadow mx-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-teal-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class="relative z=0">Get in touch &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src="images/profile.jpg"
        alt="Profile image"
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavors.
      </h6>
      <h3 class="text-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-teal-400">see</span> my work?
      </h3>
    </div>
    
    <div class="flex flex-col gap-12 mx-20 sm:flex-row sm:mx-10 md:gap-10 md:mx-20 lg:mx-30">
      <Step step={steps[0]}>
        <p>
          A lightweight e-commerce web application built with SvelteKit, TailwindCSS.
          <strong class="text-teal-400">This project demonstrates reactive state management, Svelte component structure, and responsive product pages.
          </strong>
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          This is an E-Commerce application built with Next.js, TailwindCSS, Stripe.  
          It serves as a sample store <strong class="text-teal-400">handling biotech product listing, shopping cart, and checkout flow.
             </strong>
        </p>
      </Step>
    </div>
  </section>
  <section id="about" class="py-20 pt-10 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
    <div class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-teal-700
    after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-teal-700">
        <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
        <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">A bit <span class="poppins text-teal-400">about</span> me</h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">I am . . .</p>
    <div class="flex flex-col gap-20 2-full mx-auto max-w-[800px]">
        {#each benefits as benefit, index}
            <div class="flex gap-6 sm:gap-8">
                <p class="poppins text-4xl sm:text-5sl md:text-6sl text-slate-500 font-semibold">
                    0{index+1}
                </p>
                <div class="flex flex-col gap-6 sm:gap-8">
                    <h3 class="text-2xl sm:text-3xl md:text-5xl">
                        {benefit.name}
                    </h3>
                    <p>{benefit.description}</p>
                </div>
            </div>
        {/each}
    </div>
</section>
</main>
