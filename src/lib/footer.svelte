<script>
   import { library } from '@fortawesome/fontawesome-svg-core';
   import { FontAwesomeIcon, FontAwesomeLayers, FontAwesomeLayersText } from 'fontawesome-svelte';
</script>

<footer class="bg-dark text-white pt-5">
    <div class="container">
       <div class="links row mb-5 justify-content-between">
          <div class="col-12 col-sm-6 col-md-4 d-flex flex-column">
             <h1 class="h3">Talk to us</h1>
             <a href="mailto:amartislab@gmail.com" class="my-1 text-decoration-none text-white"
                ><FontAwesomeIcon icon={['fas', 'envelope-open']} size="xs" />info@amartislab.com</a
             >
             <span class="my-1"><i class="bi bi-whatsapp text-primary me-3"></i>+256703281248</span>
             <span class="my-1"><i class="bi bi-telephone-fill text-primary me-3"></i>+256775160074</span>
          </div>
          <div class="col-12 col-sm-6 col-md-4 d-flex flex-column text-center">
             <h1 class="h3">Links</h1>
             <a href="/patners/magocreative" class="my-1 text-decoration-none text-white"><i class="bi bi-chevron-right text-success me-3"></i>Mago Media</a>
          </div>

          <div class="col-12 col-sm-6 col-md-4 text-sm-end mt-sm-0 mt-4">
             <h2 class="h3">Visit Us</h2>
             <div class="d-flex flex-column justify-content-sm-end">
                <span class="my-1">
                  <a href="instagram.com/amartislab" class="m-1 text-decoration-none text-light "
                  ><i class="bi bi-instagram text-primary me-3"></i
               >@amartislab</a>
                </span>
                <span class="my-1">
                  <a href="twitter.com/amartislab" class="m-1 text-decoration-none text-light "
                  ><i class="bi bi-twitter text-primary me-3"></i
               >@amartislab</a>
                </span>
                <span class="my-1">
                  <a href="/" class="m-1 text-decoration-none text-light ">
                     <i class="bi bi-geo-alt-fill text-primary me-3"></i>
                     Kampala, Uganda
               </a>
                </span>
             </div>
          </div>
       </div>
    </div>
    <div
       class="w-100 copy text-center p-2 bg-dark text-secondary"
    >
       All rights reserved | &copy; amarti's lab 2021
    </div>
 </footer>