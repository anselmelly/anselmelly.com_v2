<script>
    import { fade } from "svelte/transition";
    import Logo from "./partials/Logo.svelte";
    let menus = [
        {
            name: "About",
            id: "s_about",
        },
        {
            name: "Services",
            id: "s_services",
        },
        {
            name: "Clients",
            id: "s_clients",
        },
        {
            name: "Showcase",
            id: "s_showcase",
        },
        {
            name: "Experiences",
            id: "s_experiences",
        },
        {
            name: "Testimonials",
            id: "s_testimonials",
        },
        {
            name: "Contacts",
            id: "s_contacts",
        },
    ];
    $: y = 0;
    let minY = 50;
    let isOpen = false;
    $: isOpen = false;
</script>

<svelte:window bind:scrollY={y} />

<nav
    class="shadow dark:bg-gray-800 fixed top-0 left-0 right-0 z-10"
    class:bg-transparent={y < minY}
    class:bg-white={y > minY}
>
    <div
        class="container px-6 py-4 mx-auto md:flex md:justify-between md:items-center"
    >
        <div class="flex items-center justify-between">
            <Logo />

            <!-- Mobile menu button -->
            <div class="flex md:hidden">
                <button
                    on:click={() => (isOpen = !isOpen)}
                    type="button"
                    class="text-gray-500 dark:text-gray-200 hover:text-gray-600 dark:hover:text-gray-400 focus:outline-none focus:text-gray-600 dark:focus:text-gray-400"
                    aria-label="toggle menu"
                    class:text-gray-300={y < minY}
                    class:text-gray-600={y > minY}
                >
                    <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
                        <path
                            fill-rule="evenodd"
                            d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
                        />
                    </svg>
                </button>
            </div>
        </div>

        <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
        <div
            class="items-center md:flex lg:block"
            class:hidden={!isOpen}
            class:block={isOpen}
            in:fade={{ duration: 400 }}
            out:fade={{ duration: 300 }}
        >
            <div class="flex flex-col md:flex-row md:mx-6">
                {#each menus as menu}
                    <a
                        class="my-1 text-md text-right uppercase underline-offset-8 underline lg:no-underline font-bold 
                        dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0"
                        class:text-gray-300={y < minY}
                        class:text-gray-600={y > minY}
                        href="#">{menu.name}</a
                    >
                {/each}
            </div>
        </div>
    </div>
</nav>
