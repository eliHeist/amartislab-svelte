<script>
  import { onMount } from "svelte";

  onMount(() => {
    let lastScroll = 0;
    const nav = document.getElementById("navbar_top");

    document.getElementById("root").style.paddingTop = nav.offsetHeight + "px"

    window.addEventListener("scroll", () => {
      const currentScroll = window.pageYOffset;

      if (currentScroll <= 0) {
        nav.classList.remove("show");
      }
      if (currentScroll > lastScroll && !nav.classList.contains("hidden")) {
        nav.classList.remove("show");
        nav.classList.add("hidden");
      }
      if (currentScroll < lastScroll && nav.classList.contains("hidden")) {
        nav.classList.remove("hidden");
        nav.classList.add("show");
      }
      lastScroll = currentScroll;
    });
  });
</script>

<nav
  id="navbar_top"
  class="navbar fixed-top navbar-expand-lg navbar-dark bg-dark"
>
  <div class="container">
    <a class="navbar-brand" href="/">
      <img
        class="brand-img-light"
        src="/assets/logo.png"
        alt="amartislab logo"
      />
      <img
        class="brand-img-colored d-none"
        src="/assets/logo-colored.png"
        alt="amartislab logo"
      />
    </a>
    <button
      class="navbar-toggler"
      type="button"
      data-bs-toggle="collapse"
      data-bs-target="#mainNav"
    >
      <span class="navbar-toggler-icon" />
    </button>
    <div class="collapse navbar-collapse" id="mainNav">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a id="root-url" class="nav-link" href="/">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/about">About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/projects">Work</a>
        </li>
        <li class="nav-item me-2">
          <a class="nav-link" href="/services">Services</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="/contact">Contact</a>
        </li>
      </ul>
    </div>
  </div>
</nav>

<style>
  .navbar{
    transition: all .2s ease-in-out;
  }
</style>
