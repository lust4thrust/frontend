<script lang="ts">
  import { mdiFacebook, mdiInstagram, mdiYoutube } from '@mdi/js'
</script>

<div class="root">
  <a class="link" href="/" aria-label="home">
    <div class="logo" />
  </a>
  <a class="link" href="https://youtube.com/@lust4thrust" target="_blank" aria-label="youtube">
    <svg class="icon" viewBox="0 0 48 48" width="100%" height="100%">
      <path d={mdiYoutube} class="path" />
    </svg>
  </a>
  <a class="link" target="_blank" href="https://www.facebook.com/lust4thrust" aria-label="facebook">
    <svg class="icon">
      <path d={mdiFacebook} class="path" />
    </svg>
  </a>
  <a class="link" href="https://instagram.com/lust4thrust" target="_blank" aria-label="instagram">
    <svg class="icon">
      <path d={mdiInstagram} class="path" />
    </svg>
  </a>
  <div class="contact">
    <button class="button primary outline" aria-label="contact">Contact</button>
  </div>
</div>

<style>
  .root {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    width: 100%;
  }

  .logo {
    background-image: url('/img/logo.svg');
    background-size: 100% 100%;
    width: 48px;
    height: 48px;
    margin-right: 10px;
  }

  .link {
    margin-right: 10px;
  }

  .icon {
    width: 48px;
    height: 48px;
    fill: red;
  }

  .contact {
    flex: 1;
    display: flex;
    justify-content: flex-end;
  }

  .path {
    transform: scale(2.0);
  }
</style>
