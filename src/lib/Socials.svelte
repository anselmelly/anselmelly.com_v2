<script>
  let socials = [
    {
      link: "https://facebook.com/anselmelly",
      icon: '<path d="M18 2h-3a5 5 0 0 0-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 0 1 1-1h3z"/>',
      name: "Twitter",
    },
    {
      link: "https://www.linkedin.com/in/anselmelly/",
      icon: '<path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/>',
      name: "LinkedIn",
    },
    {
      link: "https://twitter/anselmelly/",
      icon: '<path d="M23 3a10.9 10.9 0 0 1-3.14 1.53 4.48 4.48 0 0 0-7.86 3v1A10.66 10.66 0 0 1 3 4s-4 9 5 13a11.64 11.64 0 0 1-7 2c9 5 20 0 20-11.5a4.5 4.5 0 0 0-.08-.83A7.72 7.72 0 0 0 23 3z"/>',
      name: "Twitter",
    },
    {
      link: "https://github.com/anselmelly/",
      icon: '<path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/>',
      name: "LinkedIn",
    },
    {
      link: "https://stackoverflow.com/story/anselmelly",
      icon: '<path d="M7.149 17.25h9.375v1.5h-9.375v-1.5z"></path><path d="M7.209 14.073l0.325-1.464 9.152 2.034-0.325 1.464-9.152-2.034z"></path><path d="M8.38 10.066l0.599-1.375 8.594 3.746-0.599 1.375-8.594-3.746z"></path><path d="M11.16 5.708l0.978-1.138 7.11 6.111-0.978 1.138-7.11-6.111z"></path><path d="M14.047 2.323l1.203-0.896 5.601 7.518-1.203 0.896-5.601-7.518z"></path><path d="M18.774 15.375v5.25h-13.875v-5.25h-1.5v6.75h16.875v-6.75h-1.5z"></path>',
      name: "Stackoverflow",
    },
  ];
  let today = new Date();
  let year = today.getFullYear();
</script>

<div class="flex justify-center items-center mt-6 pb-6">
  {#each socials as social}
    <a
      rel="noreferrer"
      href={social.link}
      class="mx-2 p-1 text-gray-300 ring-1 ring-offset-2 ring-offset-sky-600 ring-sky-600 rounded-full dark:text-gray-300 hover:text-gray-500 dark:hover:text-gray-300"
      target="_blank"
    >
      <span class="sr-only">{social.name}</span>
      <svg
        class="h-6 w-6"
        fill="currentColor"
        viewBox="0 0 24 24"
        aria-hidden="true"
      >
        {@html social.icon}
      </svg>
    </a>
  {/each}
</div>
