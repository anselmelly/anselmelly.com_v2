<script>
    import Socials from "./Socials.svelte";
    import BG from "../assets/media/pexels-roberto-nickson-2885320.jpg";
    import HImage from "../assets/media/header_image.png";
    import Nav from "./Nav.svelte";
</script>

<header
    style="background-image: url({BG})"
    class="bg-gray-700 bg-repeat-x bg-blend-overlay bg-center"
>
    <Nav />
    <div class="container px-0 py-32 mx-auto">
        <div class="items-center lg:flex lg:justify-end">
            <div
                class="flex items-center justify-center w-full mt-6 lg:mt-0 lg:w-1/2 "
            >
                <img
                    class="w-4/12 h-full lg:max-w-2xl -rotate-12 ring-sky-400 ring-2  ring-offset-4 ring-offset-sky-400 rounded-full"
                    src={HImage}
                    alt="anselmelly"
                />
            </div>
            <div class="w-full lg:w-1/2">
                <div class="lg:max-w-lg">
                    <div class="text-center">
                        <h2
                            class="text-base font-semibold text-gray-50 tracking-wide uppercase mt-8 mb-8"
                        >
                            *_*
                        </h2>
                        <div class="space-y-6">
                            <p
                                class="mt-0 text-4xl font-extrabold text-gray-50 sm:text-5xl sm:tracking-tight lg:text-6xl"
                            >
                                Hi!
                            </p>
                            <p
                                class="mt-1 text-4xl font-extrabold text-gray-50 sm:text-5xl sm:tracking-tight lg:text-6xl"
                            >
                                I am Ansel
                            </p>
                            <p
                                class="max-w-xl mt-5 mx-auto text-xl text-gray-50 mb-8"
                            >
                                Software and Web Applications Consultant
                            </p>
                        </div>

                        <Socials />
                        <div class="flex justify-between items-center">
                            <div
                                class="fb-like w-full h-full py-2 rounded-lg font-bold"
                                data-href="https://anselmelly.com"
                                data-width="450"
                                data-layout="button_count"
                                data-action="like"
                                data-size="large"
                                data-share="true"
                            />
                            <a
                                class="twitter-follow-button"
                                data-size="large"
                                href="https://twitter.com/ansymelly"
                            >
                                Follow @ansymelly</a
                            >
                            >
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</header>
