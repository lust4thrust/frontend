<div class="root">
  <iframe
    class="video"
    src="https://www.youtube.com/embed/OcqZsH9DYhg"
    frameborder="0"
    allow="web-share"
    allowfullscreen
    title="Ja sam tvoj bog"
  />
  <iframe
    class="video"
    src="https://www.youtube.com/embed/cC9tXHdJlyE"
    frameborder="0"
    allow="web-share"
    allowfullscreen
    title="Ja sam tvoj bog"
  />
</div>

<style>
  .root {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 20px;
    flex-direction: row;
  }

  .video {
    width: 50%;
    height: 315px;
  }

  @media (width < 800px) {
    .root {
      display: flex;
      align-items: center;
      justify-content: center;
      padding: 20px;
      flex-direction: column;
    }

    .video {
      width: 100%;
      height: 400px;
    }
  }
</style>
