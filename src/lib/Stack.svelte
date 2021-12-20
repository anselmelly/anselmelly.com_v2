<script>
    export let s_name = "stack";
    import {scrollRef} from 'svelte-scrolling'

    let stack = [
        {
            name: "laravel",
            logo: 'laravel.png',
            link: "https://laravel.com/",
        },

        {
            name: "wordpress",
            logo: 'wordpress.png',
            link: "https://wordpress.org/",
        },
        {
            name: "symfony",
            logo: 'symfony.png',
            link: "https://symfony.com/",
        },
        {
            name: "svelte",
            logo: 'svelte.png',
            link: "https://svelte.dev/",
        },
        {
            name: "linux (Kali)",
            logo: 'linux.png',
            link: "https://www.kali.org/",
        },
        {
            name: "tailwindcss",
            logo: 'tailwind.png',
            link: "https://tailwindcss.com/",
        },
        {
            name: "nodejs",
            logo: 'nodejs.png',
            link: "https://nodejs.org/en/",
        },
        {
            name: "netbeans",
            logo: 'netbeans_ide.jpg',
            link: "https://netbeans.apache.org/",
        },
        {
            name: "github",
            logo: 'github.png',
            link: "https://github.com/anselmelly",
        },
        {
            name: "digital_ocean",
            logo: 'digital_ocean.png',
            link: "https://www.digitalocean.com/?refcode=5fa150a1d644&utm_campaign=Referral_Invite&utm_medium=Referral_Program&utm_source=badge",
        },
    ];
</script>

<section class="p-4 m-24 mx-auto bg-white" id={s_name} use:scrollRef={s_name}>
    <div class="container mx-auto py-24 px-4 sm:px-6 lg:px-0">
        <h2 class="text-6xl font-bold mb-12">Stack</h2>
        <div class="grid grid-cols-2 gap-8 md:grid-cols-4 lg:grid-cols-5">
            {#each stack as s}
                <div
                    class="col-span-1 flex border-2 border-indigo-100 shadow-lg shadow-indigo-300 p-4 rounded-2xl justify-center md:col-span-2 lg:col-span-1"
                >
                    <a href={s.link} target="_blank">
                        <img
                            class=" w-full object-contain"
                            src='/media/stack/{s.logo}'
                            alt={s.name}
                        />
                    </a>
                </div>
            {/each}
        </div>
    </div>
</section>
