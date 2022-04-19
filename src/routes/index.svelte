<script context="module">
  export const load = async ({ fetch }) => {
    const res = await fetch('http://127.0.0.1:8000/api/projects/?format=json');
    const projects = await res.json();

    if (res.ok) {
      return {
        props: {
          projects: projects,
        },
      };
    }
    return {
      status: res.status,
      error: new Error("Could not fetch the projects"),
    };
  };
</script>

<script>
  import {
    faFacebook,
    faTwitter,
    faInstagram,
    faLinkedin,
    faWhatsapp,
  } from "@fortawesome/free-brands-svg-icons";
  import { faEnvelope } from "@fortawesome/free-solid-svg-icons";
  import HoverBtn from "$lib/components/hoverBtn.svelte";

  import { onMount } from "svelte";
  import ServiceSec from "$lib/components/home/serviceSec.svelte";
  import YChooseUs from "$lib/components/home/yChooseUs.svelte";
  import FontAwesomeIcon from "fontawesome-svelte/src/FontAwesomeIcon.svelte";
  import ProjectSec from "$lib/components/home/projectSec.svelte";
  export let projects;

  onMount(() => {
    const testimonial = document.querySelector(".slide-control.carousel-item");
    testimonial.classList.add("active");
  });
</script>

<div class="container mt-md-5 pt-5">
  <div class="row justify-content-between">
    <div class="col-12 col-lg-5 d-grid justify-content-center">
      <div class="d-grid banner-text h-100 flex-column align-center">
        <div class="catch-prase text-center text-md-start">
          <h2 class="display-3 fw-bold p-5 py-4 bg-lightdark text-white">
            Your Brand
          </h2>
          <h2 class="display-3 fw-bold p-5 py-4 bg-lightdark text-white">
            Your Story
          </h2>
        </div>
        <div class="fl1" />
        <div class="bottom mt-5 py-5">
          <ul
            class="d-flex p-3 justify-content-center justify-content-md-start bg-lightdark socials"
          >
            <a href="https://www.instagram.com/amartislab/" class="me-3 ">
              <FontAwesomeIcon icon={faInstagram} size="lg" />
            </a>
            <a href="https://twitter.com/amartislab" class="me-3 ">
              <FontAwesomeIcon icon={faTwitter} size="lg" />
            </a>
            <a href="https://wa.me/message/CHOEJPVG2LOJL1" class="me-3 ">
              <FontAwesomeIcon icon={faWhatsapp} size="lg" />
            </a>
            <a href="https://facebook.com/amartislab" class="me-3 ">
              <FontAwesomeIcon icon={faFacebook} size="lg" />
            </a>
            <a href="https://facebook.com/amartislab" class="me-3 ">
              <FontAwesomeIcon icon={faLinkedin} size="lg" />
            </a>
            <a href="mailto:amartislab@gmail.com" class="me-3 ">
              <FontAwesomeIcon icon={faEnvelope} size="lg" />
            </a>
          </ul>
          <div
            class="d-flex justify-content-center justify-content-md-start flex-column flex-sm-row mt-4"
          >
            <HoverBtn link="/services" text="Our Services" />
          </div>
        </div>
      </div>
    </div>
    <div class="col-12 col-lg-6 d-flex justify-content-end">
      <div class="bannerpic mt-auto">
        <img
          src="assets/images/bannerpic.png"
          alt="amartislab banner"
          class="w-100"
        />
      </div>
    </div>
  </div>
</div>

<ServiceSec />
<YChooseUs />
<ProjectSec {projects}/>

<section id="clients">
  <div class="container">
    <div class="d-flex" />
  </div>
</section>

<section class="testimonials py-5">
  <div class="container py-5">
    <h2 class="display-6 text-center text-white w-lg-50 mx-auto pb-5">
      What our clients say
    </h2>
    <div
      id="testimonialCarousel"
      class="carousel slide"
      data-bs-ride="carousel"
    >
      <div class="carousel-inner testimonial-divs">
        <div class="slide-control carousel-item">
          <div class="card border-0 p-5 bg-dark w-lg-50 mx-auto">
            <h2 class="name h4 text-light">
              <span class="text-primary">~</span> John Doe
            </h2>
            <p class="said lead text-altlight">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Consectetur, fuga? Quaerat quis praesentium quasi quia delectus!
            </p>
          </div>
        </div>
      </div>
      <div class="carousel-inner testimonial-divs">
        <div class="slide-control carousel-item">
          <div class="card border-0 p-5 bg-dark w-lg-50 mx-auto">
            <h2 class="name h4 text-light">
              <span class="text-primary">~</span> John Doe
            </h2>
            <p class="said lead text-altlight">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Consectetur, fuga? Quaerat quis praesentium quasi quia delectus!
            </p>
          </div>
        </div>
        <div class="slide-control carousel-item">
          <div class="card border-0 p-5 bg-dark w-lg-50 mx-auto">
            <h2 class="name h4 text-light">
              <span class="text-primary">~</span> Jane Doe
            </h2>
            <p class="said lead text-altlight">
              Lorem ipsum dolor sit amet consectetur adipisicing elit.
              Consectetur, fuga? Quaerat quis praesentium quasi quia delectus!
            </p>
          </div>
        </div>
      </div>
      <button
        class="carousel-control-prev"
        type="button"
        data-bs-target="#testimonialCarousel"
        data-bs-slide="prev"
      >
        <span class="carousel-control-prev-icon" aria-hidden="true" />
        <span class="visually-hidden">Previous</span>
      </button>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#testimonialCarousel"
        data-bs-slide="next"
      >
        <span class="carousel-control-next-icon" aria-hidden="true" />
        <span class="visually-hidden">Next</span>
      </button>
    </div>
  </div>
</section>

<style>
  .catch-prase h2 {
    width: fit-content;
    background-color: rgb(50, 50, 50);
    display: grid;
    place-items: center;
    border-radius: 0.1em;
    box-shadow: 2px 2px rgb(255, 136, 0);
    position: relative;
  }
  .catch-prase h2:nth-of-type(1) {
    z-index: 2 !important;
    transform: translateX(10px) rotateZ(-5deg);
  }
  .catch-prase h2:nth-of-type(2) {
    z-index: 1 !important;
    transform: translateX(100px) rotateZ(10deg);
  }
  @media (max-width: 500px) {
    .catch-prase h2:nth-of-type(1) {
      transform: translateX(0px) rotateZ(-5deg);
    }
    .catch-prase h2:nth-of-type(2) {
      transform: translateX(10px) rotateZ(10deg);
    }
    .w-lg-50 {
      width: 90%;
    }
  }

  .w-lg-50 {
    width: 70%;
  }
  .align-center {
    align-content: center;
  }
  .bannerpic {
    width: 100%;
    z-index: 2;
    /* position: relative; */
  }

  .bannerpic::before {
    height: 700px;
    width: 700px;
    /* border-radius: 50%; */
    position: absolute;
    z-index: 1;
    top: 0;
  }
  ul.socials {
    width: fit-content;
  }
</style>
