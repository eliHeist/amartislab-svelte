<script>
  import {faArrowRight} from '@fortawesome/free-solid-svg-icons';
import FontAwesomeIcon from 'fontawesome-svelte/src/FontAwesomeIcon.svelte';

  export let text = "Hover me";
  export let link = "#"

</script>

<a href="{link}">
  <span />
  <span />
  <span />
  <span /> {text}
  <FontAwesomeIcon icon="{faArrowRight}" size="lg"/>
</a>

<style>
  /* From uiverse.io by @menezes11 */
  a {
    position: relative;
    padding: 1em 1.8em;
    outline: none;
    border: 1px solid #303030;
    text-decoration: none;
    background: #ff9500;
    color: #303030;
    text-transform: uppercase;
    letter-spacing: 2px;
    font-size: 15px;
    overflow: hidden;
    transition: 0.2s;
    border-radius: 10px;
    cursor: pointer;
    font-weight: bold;
  }

  a:hover {
    color: white;
    box-shadow: 0 0 10px rgb(255, 136, 0), 0 0 25px #ff9500, 0 0 50px rgb(255, 136, 0);
    transition-delay: 0.6s;
    border: 1px solid #ffb700;
  }

  a span {
    position: absolute;
  }

  a span:nth-child(1) {
    top: 0;
    left: -100%;
    width: 100%;
    height: 2px;
    background: linear-gradient(90deg, transparent, #ae00ff);
  }

  a:hover span:nth-child(1) {
    left: 100%;
    transition: 0.7s;
  }

  a span:nth-child(3) {
    bottom: 0;
    right: -100%;
    width: 100%;
    height: 2px;
    background: linear-gradient(90deg, transparent, #001eff);
  }

  a:hover span:nth-child(3) {
    right: 100%;
    transition: 0.7s;
    transition-delay: 0.35s;
  }

  a span:nth-child(2) {
    top: -100%;
    right: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(180deg, transparent, #ae00ff);
  }

  a:hover span:nth-child(2) {
    top: 100%;
    transition: 0.7s;
    transition-delay: 0.17s;
  }

  a span:nth-child(4) {
    bottom: -100%;
    left: 0;
    width: 2px;
    height: 100%;
    background: linear-gradient(360deg, transparent, #001eff);
  }

  a:hover span:nth-child(4) {
    bottom: 100%;
    transition: 0.7s;
    transition-delay: 0.52s;
  }

  a:active {
    background: #ae00af;
    background: linear-gradient(to top right, #ae00af, #001eff);
    color: #bfbfbf;
    box-shadow: 0 0 8px #ae00ff, 0 0 8px #001eff, 0 0 8px #ae00ff;
    transition: 0.1s;
  }

  a:active
    span:nth-child(1)
    span:nth-child(2)
    span:nth-child(2)
    span:nth-child(2) {
    transition: none;
    transition-delay: none;
  }
</style>
