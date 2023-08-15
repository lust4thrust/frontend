<script lang="ts">
  import { mdiFacebook, mdiInstagram, mdiYoutube } from '@mdi/js'
</script>

<div class="root">
  <a href="/">
    <div class="logo" />
  </a>
  <a class="link" href="https://youtube.com/@lust4thrust" target="_blank">
    <svg class="icon">
      <path d={mdiYoutube} />
    </svg>
  </a>
  <a class="link" target="_blank" href="https://www.facebook.com/lust4thrust">
    <svg class="icon">
      <path d={mdiFacebook} />
    </svg>
  </a>
  <a class="link" href="https://instagram.com/lust4thrust" target="_blank">
    <svg class="icon">
      <path d={mdiInstagram} />
    </svg>
  </a>
  <div class="contact">
    <button class="button primary"> Contact </button>
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
    width: 26px;
    margin-right: 10px;
    height: 26px;
  }

  .link {
    width: 26px;
    height: 26px;
    margin-right: 10px;
  }

  .icon {
    width: 26px;
    height: 26px;
    fill: red;
  }

  .contact {
    flex: 1;
    display: flex;
    justify-content: flex-end;
  }
</style>
