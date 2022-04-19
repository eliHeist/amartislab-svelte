<script>
import ServiceCard from "./serviceCard.svelte";


</script>

<section id="services" class="bg-dark py-5">
    <div class="container my-5">
        <h2 class="display-6 text-center text-white w-lg-50 mx-auto pb-5">
            What we do
          </h2>
        <div class="grid d-grid">
            <ServiceCard icon="/assets/icons/webdevicon.png" title="Branding"/>
            <ServiceCard icon="/assets/icons/webdevicon.png" title="Print Design"/>
            <ServiceCard icon="/assets/icons/webdevicon.png" title="Visual Effects & Animation"/>
            <ServiceCard icon="/assets/icons/webdevicon.png" title="Product Visualisation"/>
        </div>
    </div>
</section>

<style>
    .grid{
        grid-template-columns: repeat(4, 1fr);
        gap: 1em;
    }
</style>