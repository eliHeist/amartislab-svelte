<script>
    import Navbar from '$lib/navbar.svelte'
    import Footer from '$lib/footer.svelte'

</script>

<main id="root" class="bg-altdark" style="font-family: poppins;">
    <header><Navbar/></header>
    <slot></slot>
    <Footer/>
</main>
<style>
    
</style>