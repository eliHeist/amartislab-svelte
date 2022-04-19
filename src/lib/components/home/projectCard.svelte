<script>
    export let title
    export let img
    const imgsrc = `http://127.0.0.1:8000${img}`
</script>

<article>
    <div class="img-control bg-dark">
        <img class="img-fluid" src="{imgsrc}" alt="masterpiece website">
    </div>
    <div class="more text-white">
        <h3>{title}</h3>
        <!-- <a href="./">Know more </a> -->
    </div>
</article>

<style>
    article .img-control {
  /* background-color: #1d1c1c; */
  aspect-ratio: 1/1;
  padding: 6em;
  border-radius: .5em;
  border-bottom-left-radius: .1em;
  margin-bottom: 1em;
}

article .more h3 {
  font-size: 1.2em;
  margin-bottom: .3em;
}

/* article .more a {
  text-transform: uppercase;
} */
</style>