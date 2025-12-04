<script>
  import Step from "./Step.svelte";

  let steps = [
    { name: "Biotech Store", icon: "fa-solid fa-cart-shopping" },
    { name: "Scientific Instrument Booking System", icon: "fa-solid fa-flask" },
    { name: "Chemical Matching", icon: "fa-solid fa-vial-circle-check" },
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
        href="#"
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
    <a
      href="#"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 mb-4 sm:mb-0 mt-10 hover:border-teal-700 duration-200"
    >
      <i class="fa-regular fa-circle-play"></i>
      <p>watch the video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 md:gap-10">
      <Step step={steps[0]}>
        <p>
          A modern marketplace for biotechnology supplies, cell culture
          reagents, and lab consumables. Designed for researchers and students
          needing fast, reliable ordering. <strong class="text-teal-400"
            >Smart recommendations help users find the right products quickly.</strong
          >
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          A centralized platform to reserve laboratory instruments and manage
          usage schedules. <strong class="text-teal-400"
            >Automatically syncs with calendars, sends reminders, and prevents
            booking conflicts.</strong
          > Ideal for academic labs and research facilities.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          A platform for labs to exchange surplus chemicals for ones they
          need—completely free of charge. Matches labs that have unused
          chemicals with others seeking them, creating a mutual swap system.
          <strong class="text-teal-400"
            >Helps reduce waste, lower purchasing costs, and improve resource
            sharing across institutions.</strong
          >
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
    <div class="text-2xl sm:text-3xl font-semibold text-center poppins">
        <h5>The <span class="text-teal-400 poppins">Complete</span> Package</h5>
    </div>
    <div class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full">
        <table class="bg-white text-slate-700 rounded text-center">
            <thead class="border-b border-solid border-slate-200">
                <tr class="">
                    <th/>
                    <th class="whitespace-nowrap p-2 px-4">Candidate #1</th>
                    <th class="whitespace-nowrap p-2 px-4">Candidate #2</th>
                    <th class="whitespace-nowrap p-2 px-4">Candidate #3</th>
                    <th class="whitespace-nowrap bg-teal-700 p-2 px-4">Me</th>
                </tr>
            </thead>
            <tbody>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Dedication</td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-green-500" /></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Critical Thought</td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Interpersonal Skills</td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-xmark text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
                <tr class="border-b border-solid border-slate-200">
                    <td class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm">Programming Ability</td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-slate-500" /></td>
                    <td><i class="fa-solid fa-check text-green-500" /></td>
                </tr>
            </tbody>
        </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
        <p>Scroll to see more &rarr;</p>
    </div>
</section>
</main>
