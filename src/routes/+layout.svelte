<script>
  import 'chota'
  import { store } from '@freenit-framework/svelte-base'
  import { SvelteToast } from '@zerodevx/svelte-toast'
  import './styles.css'

  const options = {}

  // First invocation of this function creates store, next invocations return
  // existing one, so only first invocation takes "prefix" argument into account
  store('/api/v1')
</script>

<svelte:head>
  <title>Lust 4 Thrust</title>
  <meta name="Lust4Thrust" content="Lust 4 Thrust" />
</svelte:head>

<SvelteToast {options} />
<div class="main">
  <slot />
</div>

<style>
  .main {
    height: 100vh;
    width: 100vw;
  }
</style>
