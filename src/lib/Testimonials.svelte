<script>
    export let s_name = "testimonials";
    import {scrollRef} from 'svelte-scrolling'
    let testimonials = [
        {
            name: "Huston Malande",
            url: "https://www.linkedin.com/in/hustonmalande/",
            title: "CEO, Skyline",
            text: "Ansel is an exceptional developer: honest and trustworthy, has technical depth and breadth of experience, and is the essential kind of project hacker who figures things out and gets them to work by any means necessary. I highly recommend him.",
        },
        {
            name: "Brian Ngaira",
            url: "https://www.linkedin.com/in/brian-ngaira-b21b8871/",
            title: "Managing Director, Web Afriq",
            text: "Projects are enjoyable when working with a skilled, talented, reliable problem solver. That is working with Ansel Melly",
        },
        {
            name: "Vitalis K'omudho",
            url: "https://www.linkedin.com/in/vitalis-komudho-234b2658/",
            title: "CEO, Sienna Insurance",
            text: "Knowing Ansel over the last five years in our operations as an organization has made our life much easier on matters software development! An experienced & easy going chap who doesn't get annoyed regardless of the number of times his services may be required in a day! Ansel Melly, he is!",
        },
        {
            name: "Bonita Aluoch",
            url: "https://www.pinterest.com/BonitaonSafari/_created/",
            title: "Travel Blogger and photographer",
            text: "Ansel is the most reliable,sensible and honest tech guy I have ever worked with. He is a kind and patient problem solver who always a phone or email away. Working with him for more than four years now has been a delightful journey and would recommend him over and over again. Pay him all your monies and get the much needed peace of mind and confidence in your tech stuff.",
        },
    ];
</script>

<section class="p-4 m-24 mx-auto bg-gray-200" id={s_name} use:scrollRef={s_name}>
    <div class="p-4 m-4 container mx-auto">
        <h2 class="text-6xl font-bold mb-12">Testimonials</h2>
        <div class="container mx-auto px-4">
            <div class="md:flex md:flex-wrap mb-4">
                {#each testimonials as testimonial}
                    <div class="md:w-1/2 md:px-4 mt-6">
                        <div
                            class="bg-white shadow-sm rounded-xl p-6 border-2 border-solid flex hover:border-gray-400 hover:bg-gray-100 transition-colors duration-300"
                        >
                            <div
                                class="w-12 h-12 md:w-20 md:h-20 text-indigo-800 rounded-full overflow-hidden mr-4 md:mr-6 flex-shrink-0"
                            >
                                <svg
                                    xmlns="http://www.w3.org/2000/svg"
                                    class="h-full w-full"
                                    fill="none"
                                    viewBox="0 0 24 24"
                                    stroke="currentColor"
                                >
                                    <path
                                        stroke-linecap="round"
                                        stroke-linejoin="round"
                                        stroke-width="2"
                                        d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z"
                                    />
                                </svg>
                            </div>
                            <div>
                                <p class="text-gray-600">
                                    {@html testimonial.text}
                                </p>
                                <div
                                    class="text-sky-900 font-bold uppercase mt-6"
                                >
                                    <a href={testimonial.url} target="_blank">
                                        - {testimonial.name}.
                                    </a>
                                </div>
                                <div class="text-sky-600">
                                    {testimonial.title}
                                </div>
                            </div>
                        </div>
                    </div>
                {/each}
            </div>
        </div>
    </div>
</section>
