<script>
  export let text = "Hover me";
  export let link = "#";
  export let classes;
</script>

<a href={link} class="cta {classes}" type="submit">
  <span>{text}</span>
  <svg viewBox="0 0 13 10" height="10px" width="15px">
    <path d="M1,5 L11,5" />
    <polyline points="8 1 12 5 8 9" />
  </svg>
</a>

<style>
  /* From uiverse.io by @alexmaracinaru */
  .cta {
    position: relative;
    /* margin: auto; */
    padding: .5em 1em 1em 1em;
    transition: all 0.2s ease;
    border: none;
    background: none;
    text-decoration: none;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .cta:before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    display: block;
    border-radius: 50px;
    background: #00d9ff;
    width: 45px;
    height: 45px;
    transition: all 0.3s ease;
  }

  .cta span {
    position: relative;
    font-size: 1.2em;
    font-weight: 400;
    letter-spacing: 0.05em;
    color: rgb(255, 255, 255);
  }

  .cta svg {
    position: relative;
    top: 0;
    margin-left: 10px;
    fill: none;
    stroke-linecap: round;
    stroke-linejoin: round;
    stroke: #00d9ff;
    stroke-width: 2;
    transform: translateX(-5px);
    transition: all 0.3s ease;
  }

  .cta:hover:before {
    width: 100%;
    background: #00d9ff;
  }

  .cta:hover svg {
    transform: translateX(0);
    stroke: rgb(255, 255, 255);
  }

  .cta:active {
    transform: scale(0.95);
  }
</style>
