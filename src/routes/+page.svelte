<script lang="ts">
  import Albumi from '$lib/landing/Albumi.svelte'
  import Header from '$lib/landing/Header.svelte'
  import Svirke from '$lib/landing/Svirke.svelte'
  import Spotovi from '$lib/landing/Spotovi.svelte'
  import Footer from '$lib/landing/Footer.svelte'
  import band from '$lib/img/band.jpg'

  let innerWidth = 1024
</script>

<svelte:window bind:innerWidth />

<div class="root">
  <div class="first" style={`background-image: url(${band})`}>
    <Header />
    <div class="content" class:content-small={innerWidth < 800}>
      {#if innerWidth < 800}
        <h1 class="title">Lust</h1>
        <h1 class="title">4</h1>
        <h1 class="title">Thrust</h1>
      {:else}
        <h1 class="title">Lust 4 Thrust</h1>
      {/if}
    </div>
  </div>
  <Albumi />
  <Svirke />
  <Spotovi />
  <Footer />
</div>

<style>
  .root {
    min-height: 100vh;
    background-color: #171320;
    color: #deddda;
  }

  .first {
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-size: 100% 100%;
  }

  .content {
    flex: 1;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .content-small {
    flex-direction: column;
    line-height: 1rem;
  }

  .title {
    font-size: 8rem;
    color: var(--color-primary);
  }
</style>
