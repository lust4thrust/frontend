<script lang="ts">
  import {
    mdiPause,
    mdiPlay,
    mdiRepeat,
    mdiRepeatOff,
    mdiSkipNextOutline,
    mdiSkipPreviousOutline,
  } from '@mdi/js'

  let innerWidth = 1024
  let index = 0
  let repeat = false
  let play = false
  let player: HTMLAudioElement
  let duration = 0
  let currentTime = 0
  let time = '00:00 / 00:00'
  let volume = 100
  const albums = [
    {
      title: 'Da li si spremna za let?',
      songs: [
        { title: 'Da li si spremna za let?', file: '01 da li si spremna za let' },
        { title: 'Kriza morala', file: '02 kriza morala' },
        { title: 'Ja sam tvoj Bog', file: '03 ja sam tvoj bog' },
        { title: 'Zver u tebi', file: '04 zver u tebi' },
        { title: 'Plen', file: '05 plen' },
        { title: 'Tvorac', file: '06 tvorac' },
        { title: 'Poslednji pozdrav', file: '07 poslednji pozdrav' },
        { title: 'Manifestacija uma', file: '08 manifestacija uma' },
        { title: 'Veselje neka počne', file: '09 veselje neka počne' },
        { title: 'Leader', file: '10 leader' },
      ],
    },
  ]
  let url = `/data/${albums[0].songs[0].file}.ogg`

  function previous() {
    --index
    if (index < 0) {
      if (repeat) {
        index = albums[0].songs.length - 1
      } else {
        index = 0
      }
    }
    url = `/data/${albums[0].songs[index].file}.ogg`
  }

  function next() {
    ++index
    if (index >= albums[0].songs.length) {
      if (repeat) {
        index = 0
      } else {
        index = albums[0].songs.length
      }
    }
    url = `/data/${albums[0].songs[index].file}.ogg`
  }

  function togglePlay() {
    if (player.paused) {
      player.play()
    } else {
      player.pause()
    }
    play = !player.paused
  }

  function timeChanged() {
    currentTime = player.currentTime
    time = `${calculateTime(currentTime)} / ${calculateTime(duration)}`
  }

  function metaLoaded() {
    duration = player.duration
    time = `${calculateTime(currentTime)} / ${calculateTime(duration)}`
  }

  function calculateTime(secs: number) {
    const minutes = Math.floor(secs / 60)
    const seconds = Math.floor(secs % 60)
    const returnedSeconds = seconds < 10 ? `0${seconds}` : `${seconds}`
    return `${minutes}:${returnedSeconds}`
  }

  function changeVolume(event: Event) {
    const target = event.target as HTMLInputElement
    volume = Number(target.value)
    player.volume = volume / 100
  }

  function changeTime(event: Event) {
    const target = event.target as HTMLInputElement
    currentTime = Number(target.value)
    player.currentTime = currentTime
  }

  function toggleRepeat() {
    repeat = !repeat
  }

  $: icon = play ? mdiPause : mdiPlay
  $: repeatIcon = repeat ? mdiRepeat : mdiRepeatOff
</script>

<svelte:window bind:innerWidth />

<div class="root">
  <div class="title">{albums[0].songs[index].title}</div>
  <div class="player">
    <audio
      autoplay={play}
      src={url}
      on:ended={next}
      bind:this={player}
      preload="metadata"
      on:timeupdate={timeChanged}
      on:loadedmetadata={metaLoaded}
    />
    <button class="button clear" on:click={previous}>
      <svg class="play">
        <path d={mdiSkipPreviousOutline} />
      </svg>
    </button>
    <button class="button clear" on:click={togglePlay}>
      <svg class="play">
        <path d={icon} />
      </svg>
    </button>
    <button class="button clear" on:click={next}>
      <svg class="play">
        <path d={mdiSkipNextOutline} />
      </svg>
    </button>
    <input
      class="time-slider"
      type="range"
      min={0}
      max={duration}
      value={currentTime}
      on:input={changeTime}
    />
    {#if innerWidth > 800}
      <input
        class="volume"
        type="range"
        min={0}
        max={100}
        value={volume}
        on:input={changeVolume}
      />
    {/if}
    <p class="time">{time}</p>
    <button class="button clear repeat" on:click={toggleRepeat}>
      <svg class="play" class:disabled={!repeat}>
        <path d={repeatIcon} />
      </svg>
    </button>
  </div>
</div>

<style>
  .root {
    position: sticky;
    bottom: 0;
    border-width: 1px;
    border-style: solid;
    border-color: rgb(100, 0, 0);
  }

  .title {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .play {
    width: 25px;
    height: 22px;
    fill: red;
  }

  .button {
    padding: 0;
    margin-left: 10px;
  }

  .player {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .volume {
    width: 100px;
  }

  .time {
    margin: 0;
    margin-left: 20px;
  }

  .time-slider {
    flex: 1;
    margin-left: 20px;
    margin-right: 20px;
  }

  input[type='range'] {
    accent-color: red;
  }

  .disabled {
    fill: gray;
  }

  .repeat {
    margin-right: 20px;
  }
</style>
