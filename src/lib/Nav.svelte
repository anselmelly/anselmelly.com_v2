<script>
    import { scrollElement, setGlobalOptions } from "svelte-scrolling";

    import { quadInOut } from "svelte/easing";
    import { fade } from "svelte/transition";
    import Logo from "./partials/Logo.svelte";
    let options = {
        duration: 800,
        offset: -60,
        easing: quadInOut,
    };
    let globalOptions = setGlobalOptions(options);
    let menus = [
        {
            name: "About",
            id: "about",
        },
        {
            name: "Stack",
            id: "stack",
        },
        {
            name: "Services",
            id: "services",
        },
        
        {
            name: "Showcase",
            id: "showcase",
        },
        {
            name: "Clients",
            id: "clients",
        },
        {
            name: "Testimonials",
            id: "testimonials",
        },
        {
            name: "Contacts",
            id: "contacts",
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
                        on:click|preventDefault={(e) => {
                            scrollElement(menu.id);
                            isOpen = !isOpen;
                        }}
                        class="my-1 text-md text-right uppercase underline-offset-8 underline lg:no-underline font-bold
                        dark:text-gray-200 hover:text-blue-500 dark:hover:text-blue-400 md:mx-4 md:my-0 inline-block h-6"
                        class:text-gray-300={y < minY}
                        class:text-gray-600={y > minY}
                        href="#{menu.id}"
                    >
                        <span class="inline-block">
                            {menu.name}
                        </span>
                    </a>
                {/each}
            </div>
        </div>
    </div>
</nav>
