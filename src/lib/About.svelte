<script>
  import {scrollRef} from 'svelte-scrolling'
  let h = [
    {
      title: "Experience",
      details: "10+ Years",
    },
    {
      title: "Clients",
      details: "50+ Clients",
    },
    {
      title: "Projects",
      details: "30+ Projects Completed",
    },
    {
      title: "Teams",
      details: "5+ Teams",
    },
  ];
</script>

<section class="p-4 m-24 container mx-auto" use:scrollRef={'about'} id='about'>
  <h2 class="text-6xl font-bold mb-12">About Me</h2>
  <div class="flex flex-col  lg:flex-row ">
    <div class=" align-bottom lg:w-1/3">
      <div
        class="flex flex-row flex-wrap lg:flex-col items-start justify-between lg:w-full"
      >
        {#each h as hi}
          <div
            class="flex flex-col text-center p-4 rounded bg-gray-100 basis-1/2 lg:basis-full lg:w-full lg:mb-2 lg:text-right"
          >
            <span class="font-extralight  text-xs uppercase">{hi.title}</span>
            <span class="font-bold text-lg capitalize">{@html hi.details}</span>
          </div>
        {/each}

        <div />
      </div>
    </div>
    <div class=" border-gray-400 pl-2  lg:w-2/3">
      <div
        class="prose prose-indigo prose-lg max-w-prose w-full text-gray-600 lg:max-w-2xl md:text-left text-xl lg:pl-8"
      >
        <p>
          I am a software and web applications consultant with vast experience
          in building usable applications.
        </p>
        <p>
          I have been actively developing software applications for close to 10
          years with a passion for technology, especially when applied to
          problem-solving real-life problems.
        </p>
        <p>I have worked on several projects with clients and teams to achieve their goals.</p>

        <p>
          I have also worked on personal projects that have enabled me to further gain relevant knowledge
        </p>
        <p>
          From time to time I work with teams to complete projects for clients. This provides me with an added 
          advantage undestanding  team dynamics
        </p>
      </div>
    </div>
  </div>
</section>
