<script lang="ts">
  import { mdiFacebook, mdiInstagram, mdiYoutube } from '@mdi/js'
</script>

<div class="root">
  <div class="social">
    <a href="/">
      <div class="logo" />
    </a>
    <a class="link" href="https://youtube.com/@lust4thrust" target="_blank">
      <svg class="icon">
        <path d={mdiYoutube} />
      </svg>
    </a>
    <a class="link" href="https://www.facebook.com/lust4thrust" target="_blank">
      <svg class="icon">
        <path d={mdiFacebook} />
      </svg>
    </a>
    <a class="link" href="https://instagram.com/lust4thrust" target="_blank">
      <svg class="icon">
        <path d={mdiInstagram} />
      </svg>
    </a>
  </div>
  <div class="colfJsDB">Lust 4 Thrust</div>
  <div class="rights">All rights reserved</div>
</div>

<style>
  .root {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 10px;
    width: 100%;
  }

  .social {
    flex: 1;
    display: flex;
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

  .rights {
    flex: 1;
    display: flex;
    justify-content: flex-end;
  }
</style>
