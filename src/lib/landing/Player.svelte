<script lang="ts">
  import { mdiPause, mdiPlay } from '@mdi/js'

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
        { title: 'Da li si spremna za let?', file: 'da li si spremna za let' },
        { title: 'Kriza morala', file: 'kriza morala' },
        { title: 'Ja sam tvoj Bog', file: 'ja sam tvoj bog' },
        { title: 'Zver u tebi', file: 'zver u tebi' },
        { title: 'Plen', file: 'plen' },
        { title: 'Tvorac', file: 'tvorac' },
        { title: 'Poslednji pozdrav', file: 'poslednji pozdrav' },
        { title: 'Manifestacija uma', file: 'manifestacija uma' },
        { title: 'Veselje neka počne', file: 'veselje neka počne' },
        { title: 'Leader', file: 'leader' },
      ],
    },
  ]
  let url = `/data/${albums[0].songs[0].file}.ogg`

  function next() {
    ++index
    if (repeat) {
      index = index / albums[0].songs.length
    }
    if (index < albums[0].songs.length) {
      url = `/data/${albums[0].songs[index].file}.ogg`
    }
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

  $: icon = play ? mdiPause : mdiPlay
</script>

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
    <button class="button clear" on:click={togglePlay}>
      <svg class="play">
        <path d={icon} />
      </svg>
    </button>
    <input
      class="time-slider"
      type="range"
      max={duration}
      value={currentTime}
      on:input={changeTime}
    />
    <input
      class="volume"
      type="range"
      max={100}
      value={volume}
      on:input={changeVolume}
    />
    <p class="time">{time}</p>
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
    height: 20px;
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
    margin-right: 20px;
  }

  .time-slider {
    flex: 1;
    margin-left: 20px;
    margin-right: 20px;
  }

  input[type='range'] {
    accent-color: red;
  }
</style>
