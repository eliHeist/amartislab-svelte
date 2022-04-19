<script>
	import SendBtn from '$lib/components/sendBtn.svelte';
</script>

<div class="contacts mb-5">
    <div class="container">
       <div class="row">
          <div class="
                 col-lg-4 col-md-6 col-sm-12
                 justify-content-center
                 justify-content-lg-start
                 justify-content-md-start
                 my-3
                 fade-in
                 slide-in
                 from-left
              ">
             <div class="
                    card
                    bg-dark
                    p-4
                    d-grid
                    flex-column
                    justify-content-center
                    align-items-top
                    text-center
                    h-100
                 ">
                <div class="textcenter icon mb-4">
                   <i class="bi bi-phone-fill display-1 text-alt"></i>
                </div>
                <h2 class="h5 text-primary">Call Us</h2>
                <div class="body">
                   <p class="text-light">+256 703281248</p>
                   <p class="text-light">+256 775160074</p>
                </div>
             </div>
          </div>
          <div class="
                 col-lg-4 col-md-6 col-sm-12
                 justify-content-center
                 justify-content-lg-center
                 justify-content-md-end
                 my-3
                 fade-in
              ">
             <div class="
                    card
                    bg-dark
                    p-4
                    d-grid
                    flex-column
                    justify-content-center
                    align-items-top
                    text-center
                    h-100
                 ">
                <div class="textcenter icon">
                   <img src="assets/qrcode.jfif" alt="whatsapp chat code" class="img-fluid">
                </div>
                <p>
                   Scan code to chat
                </p>
             </div>
          </div>
          <div class="
                 col-lg-4 col-md-12 col-sm-12
                 justify-content-center
                 justify-content-lg-end
                 justify-content-md-start
                 my-3
                 fade-in
                 slide-in
                 from-right
              ">
             <div class="
                    card
                    bg-dark
                    p-4
                    d-grid
                    flex-column
                    justify-content-center
                    align-items-top
                    text-center
                    h-100
                 ">
                <div class="textcenter icon mb-4">
                   <i class="bi bi-chat-fill display-1 text-alt"></i>
                </div>
                <h2 class="h5 text-primary">
                   Visit us on Social Media
                </h2>
                <div class="body">
                   <p class="">
                      <a href="https://www.instagram.com/amartislab/" class="text-decoration-none text-light"><i
                            class="bi bi-instagram text-white me-3"></i>@amartislab
                      </a>
                   </p>
                   <p class="">
                      <a href="https://twitter.com/amartislab" class="text-decoration-none text-light"><i
                            class="bi bi-twitter text-white me-3"></i>@amartislab
                      </a>
                   </p>
                </div>
             </div>
          </div>
       </div>
    </div>
 </div>

 <div class="container py-5 mb-5">
    <div class="width mx-auto row align-items-center justify-content-center row-contact">
        <div class="col col-10 col-md-5 col-lg-4 px-0">
            <address class="p-5 bg-primary">
                <h1 class="fs-2">Contact US</h1>
                <ul class="list-unstyled lead">
                    <li class="py-3 w-100"><i class="me-3 fas fa-envelope"></i>info@amartislab.com</li>
                    <li class="py-3"><i class="me-3 fas fa-phone-alt"></i>+256 703 281 248</li>
                    <li class="py-3"><i class="me-3 fas fa-phone-alt"></i>+256 775 160 074</li>
                </ul>
            </address>
        </div>
        <div class="col col-12 col-md-7 col-lg-8 px-0">
            <form action="#" class="bg-dark p-5">
                <main>
                    <h2 class="display-6 text-white">Get in touch</h2>
                    <p class="form-text">Feel free to drop a message below</p>
                    <div class="form-floating mb-3">
                        <input type="text" class="form-control bg-altdark border-altdark" name="name" id="name" placeholder="John Doe">
                        <label for="floatingInput" class="text-muted">Name</label>
                      </div>
                    <div class="form-floating mb-3">
                        <input type="email" class="form-control bg-altdark border-altdark" name="email" id="email" placeholder="name@example.com">
                        <label for="floatingInput" class="text-muted">Email address</label>
                      </div>
                    <div class="form-floating mb-3">
                        <textarea class="form-control bg-altdark border-altdark" name="message" id="message" placeholder="message" rows="5"></textarea>
                        <label for="floatingInput" class="text-muted">Message</label>
                      </div>
                    <SendBtn/>
                </main>
            </form>
        </div>
    </div>
</div>

<style>
    .row-contact{
        background: linear-gradient(to bottom, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 17%, rgb(14, 14, 14) 17%, rgb(14, 14, 14) 100%);
    }
    @media (min-width: 768px){
        .row-contact{
            background: linear-gradient(to right, rgba(0,0,0,0) 0%, rgba(0,0,0,0) 20%, rgb(14, 14, 14) 20%, rgb(14, 14, 14) 100%);
        }
    }
    #message{
        min-height: 150px;
    }
    .width{
       width: 80%;
    }
</style>