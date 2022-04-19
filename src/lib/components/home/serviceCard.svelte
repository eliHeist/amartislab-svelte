<script>
    export let title = 'Title';
    export let icon = '/assets/home-banner.png';
</script>

<figure class="text-white">
    <div class="img-control mx-auto mb-4 mt-3">
        <img src="{icon}" alt="{title}" class="mx-auto">
    </div>
  <h3 class="title">{title}</h3>
</figure>

<style>
  figure {
    aspect-ratio: 1/1;
    background-color: #1d1c1c;
    padding: 1.8em;
    border-radius: 2em;
  }

  figure .img-control{
      aspect-ratio: 1/1;
      background-color: #100f0f;
      border-radius: 50%;
      display: grid;
      place-content: center;
      width: 50%;
  }

  img{
      max-width: 70%;
  }

  figure .title {
    font-size: 1.6em;
    margin-bottom: 0.5em;
    text-align: center;
  }
</style>
