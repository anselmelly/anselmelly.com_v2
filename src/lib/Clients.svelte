<script>
    import { onMount } from "svelte";

    export let s_name = "clients";
    import { scrollRef } from "svelte-scrolling";
    let clients = [
        {
            name: "BAKE",
            url: "https://bake.co.ke",
            logo: "bake.png",
            bg: "bg-gray-200",
        },
        {
            name: "Bonitta",
            url: "https://aluochbonnita.com/",
            logo: "bonnita.png",
            bg: "bg-gray-200",
        },
        {
            name: "Mukuru Stoves",
            url: "https://mukurustoves.org/",
            logo: "mukuru.png",
            bg: "bg-gray-200",
        },
        {
            name: "Hapakenya",
            url: "https://hapakenya.com/",
            logo: "hapakenya.png",
            bg: "bg-gray-200",
        },
        {
            name: "Zenevan Consulting",
            url: "https://zenevan.co.ke/",
            logo: "zenevan.png",
            bg: "bg-black",
        },
        {
            name: "Cherehani Africa",
            url: "https://cherehani.org/",
            logo: "cherehani.png",
            bg: "bg-black",
        },

        {
            name: "Sienna Insurance",
            url: "http://siennainsurance.co.ke/",
            logo: "sienna.png",
            bg: "bg-black",
        },
        {
            name: "East African Engeneering Consultants",
            url: "https://eaecgroup.com/",
            logo: "eaecgroup.png",
            bg: "bg-black",
        },
    ];
    onMount(async () => {
        clients.forEach(async (client, k) => {
            let logo = 'media/clients/' + client.logo;
            clients[k].ilogo = logo;
        });
    });
</script>

<section class="p-12 m-24 bg-white  mx-auto" use:scrollRef={s_name} id={s_name}>
    <div class="container px-6 py-0 mx-auto">
        <div class="grid grid-cols-1 gap-8 md:grid-cols-4 lg:grid-cols-4">
            {#each clients as client}
                <div
                    class="flex items-center border-2 {client.bg} rounded justify-center col-span-1 md:col-span-2 lg:col-span-1"
                >
                    <img
                        class=" object-contain"
                        src={client.ilogo}
                        alt={client.name}
                    />
                </div>
            {/each}
        </div>
    </div>
</section>
