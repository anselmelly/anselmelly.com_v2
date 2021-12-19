<script>
  import About from "./lib/About.svelte";
  import Contacts from "./lib/Contacts.svelte";
import Footer from "./lib/Footer.svelte";
  import Header from "./lib/Header.svelte";
  import Cta from "./lib/partials/CTA.svelte";
  import Services from "./lib/Services.svelte";
  import Stack from "./lib/Stack.svelte";
  import TailwindStyles from "./lib/TailwindCSS.svelte";
  import Testimonials from "./lib/Testimonials.svelte";
</script>

<main>
  <!-- This example requires Tailwind CSS v2.0+ -->
  <div class="max-w-full mx-auto ">
    <Header />
    <About />
    <Cta />
    <Stack />
    <Services />
    <Testimonials />
    <Contacts />
    <Footer/>
  </div>
</main>
