<script>
    export let s_name = "stack";
    import {scrollRef} from 'svelte-scrolling'
    import laravel from "../assets/media/stack/laravel.png";
    import wordpress from "../assets/media/stack/wordpress.png";
    import symfony from "../assets/media/stack/symfony.png";
    import svelte from "../assets/media/stack/svelte.png";
    import linux from "../assets/media/stack/linux.png";
    import tailwind from "../assets/media/stack/tailwind.png";
    import nodejs from "../assets/media/stack/nodejs.png";
    import netbeans from "../assets/media/stack/netbeans_ide.jpg";
    import github from "../assets/media/stack/github.png";
    import digitalOcean from "../assets/media/stack/digital_ocean.png";

    let stack = [
        {
            name: "laravel",
            logo: laravel,
            link: "https://laravel.com/",
        },

        {
            name: "wordpress",
            logo: wordpress,
            link: "https://wordpress.org/",
        },
        {
            name: "symfony",
            logo: symfony,
            link: "https://symfony.com/",
        },
        {
            name: "svelte",
            logo: svelte,
            link: "https://svelte.dev/",
        },
        {
            name: "linux (Kali)",
            logo: linux,
            link: "https://www.kali.org/",
        },
        {
            name: "tailwindcss",
            logo: tailwind,
            link: "https://tailwindcss.com/",
        },
        {
            name: "nodejs",
            logo: nodejs,
            link: "https://nodejs.org/en/",
        },
        {
            name: "netbeans",
            logo: netbeans,
            link: "https://netbeans.apache.org/",
        },
        {
            name: "github",
            logo: github,
            link: "https://github.com/anselmelly",
        },
        {
            name: "digital_ocean",
            logo: digitalOcean,
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
                    class="col-span-1 flex border-2 border-green-500 p-4 rounded-2xl justify-center md:col-span-2 lg:col-span-1"
                >
                    <a href={s.link} target="_blank">
                        <img
                            class="h-32 w-3/4 object-contain"
                            src={s.logo}
                            alt={s.name}
                        />
                    </a>
                </div>
            {/each}
        </div>
    </div>
</section>
