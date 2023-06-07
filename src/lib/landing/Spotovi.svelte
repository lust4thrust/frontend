<div class="root">
  <div class="content">
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
      title="Plen"
    />
  </div>
</div>

<style>
  .root {
    padding: 20px;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .content {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    width: 100%;
    max-width: 1024px;
  }

  .video {
    width: 50%;
    height: 315px;
  }

  @media (width < 1024px) {
    .content {
      display: flex;
      align-items: center;
      justify-content: center;
      flex-direction: column;
      width: 100%;
    }

    .video {
      width: 100%;
      height: 400px;
    }
  }
</style>
