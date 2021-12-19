<script>
  import About from "./lib/About.svelte";
  import Clients from "./lib/Clients.svelte";
  import Contacts from "./lib/Contacts.svelte";
  import Footer from "./lib/Footer.svelte";
  import Header from "./lib/Header.svelte";
  import Cta from "./lib/partials/CTA.svelte";
  import Fb from "./lib/partials/FB.svelte";
  import Meta from "./lib/partials/Meta.svelte";
  import Twit from "./lib/partials/Twit.svelte";
  import Services from "./lib/Services.svelte";
  import Showcase from "./lib/Showcase.svelte";
  import Stack from "./lib/Stack.svelte";
  import TailwindStyles from "./lib/TailwindCSS.svelte";
  import Testimonials from "./lib/Testimonials.svelte";
</script>

<Meta />
<main>
  <Fb />
  <Twit />
  <div class="max-w-full mx-auto ">
    <Header />
    <About />
    <Cta />
    <Stack />
    <Services />
    <Showcase />
    <Clients />
    <Testimonials />
    <Contacts />
    <Footer />
  </div>
</main>
