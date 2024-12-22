<script lang="ts">
  import { writable } from 'svelte/store'

  let showPlen = writable(false)
  let showBog = writable(false)

  function show(video: string) {
    function doShow() {
      if (video === 'plen') {
        $showPlen = true
      } else {
        $showBog = true
      }
    }
    return doShow
  }
</script>


<div class="root">
  <div class="content">
    {#if $showPlen}
      <iframe
        class="video"
        src="https://www.youtube.com/embed/OcqZsH9DYhg?autoplay=1"
        frameborder="0"
        allow="autoplay web-share"
        allowfullscreen
        title="Plen"
      />
    {:else}
      <div class="video plen" on:click={show('plen')} on:keypress={show('plen')} />
    {/if}
    {#if $showBog}
      <iframe
        class="video"
        src="https://www.youtube.com/embed/cC9tXHdJlyE?autoplay=1"
        frameborder="0"
        allow="autoplay web-share"
        allowfullscreen
        title="Ja sam tvoj bog"
      />
    {:else}
      <div class="video bog" on:click={show('bog')} on:keypress={show('plen')} />
    {/if}
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

  .plen {
    background-image: url('/img/plen-spot.webp');
    background-repeat: no-repeat;
    background-size: 100% 100%;
  }

  .bog {
    background-image: url('/img/bog-spot.webp');
    background-repeat: no-repeat;
    background-size: 100% 100%;
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
