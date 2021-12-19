<script>
    export let s_name = 'services';
    import {scrollRef} from 'svelte-scrolling'
    let services = [
        {
            title:"Web Development",
            description:"Creating beautiful, intuitive and responsive websites to make you stand out online through leveraging latest and upto date technologies e.g tailwindcss, nodejs, laravel",
            icon:'  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z" />'
        },
        {
            title:"Wordpress Development",
            description:"Wordpress is a battle tested CSM platform used to manage content e.g blogs and website. Themeing and plugin development for wordpress is where I come in.",
            icon:'  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />'
        },
        {
            icon:'  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 9l3 3-3 3m5 0h3M5 20h14a2 2 0 002-2V6a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />',
            title:"Server Management",
            description:"Always on standby to keep your website up and running 99.9% of the time: Security updates and patches, troubleshooting, and content management."
        },
        {
            icon:'<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />',
            title:"Software Development",
            description:"Developing and supporting custom software applications to enable you engage with your clients in realtime from any location. e.g e-commerce"
        },
        {
            icon:'  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z" />',
            title:"Technical support",
            description:"Technical advice or guidance for your technical team on how to troubleshoot your website or technology stack and have you running in no time."
        },
        {
            icon:'  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 10h.01M12 10h.01M16 10h.01M9 16H5a2 2 0 01-2-2V6a2 2 0 012-2h14a2 2 0 012 2v8a2 2 0 01-2 2h-5l-5 5v-5z" />',
            title:"Technical advisory",
            description:"Being a technical advisory for organizations or individuals on relevant technologies currently for communication and customer support"
        }
    ];
</script>
<section class="p-4 m-24 mx-auto bg-indigo-500" id={s_name} use:scrollRef={s_name}>
    <div class=" container py-2 mx-auto m-24 p-8">
        <h2 class="text-6xl font-bold mb-12 text-white">Services...</h2>
        <p class="text-white text-xs uppercase">...what I endevor to offer the clients</p>
        <div
            class="mx-auto px-4 text-center sm:max-w-3xl sm:px-6 lg:px-8 lg:max-w-7xl"
        >
            <div class="mt-12">
                <div
                    class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-3"
                >
                {#each services as service}
                    <div class="pt-6">
                        <div class="flow-root bg-gray-50 rounded-lg px-6 pb-8">
                            <div class="-mt-6">
                                <div>
                                    <span
                                        class="inline-flex items-center justify-center p-3 bg-indigo-500 rounded-md shadow-lg"
                                    >
                                        <!-- Heroicon name: outline/cloud-upload -->
                                        <svg
                                            class="h-6 w-6 text-white"
                                            xmlns="http://www.w3.org/2000/svg"
                                            fill="none"
                                            viewBox="0 0 24 24"
                                            stroke="currentColor"
                                            aria-hidden="true"
                                        >
                                            {@html service.icon??''}
                                        </svg>
                                    </span>
                                </div>
                                <h3
                                    class="mt-8 text-lg font-medium text-gray-900 tracking-tight"
                                >
                                    {service.title}
                                </h3>
                                <div class="prose prose-xl">
                                    <p class="mt-5 text-lg text-gray-500">
                                        {@html service.description}
                                    </p>
                                </div>
                                
                            </div>
                        </div>
                    </div>
                    {/each}

                    
                </div>
            </div>
        </div>
    </div>
</section>
