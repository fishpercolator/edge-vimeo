<template>
  <div class="container">
    <div class="card vimeo-example">
      <div class="card-image">
        <div class="vimeo-example__embed">
          <vimeo-player ref="player" :video-id="346437994" :options="vimeoOptions" v-on:play="isPlaying = true" v-on:ended="isPlaying = false" />
        </div>
      </div>
      <div class="card-content">
        <button v-if="!isPlaying" class="button is-primary" @click="$refs.player.play()">Play</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      isPlaying: false,
      vimeoOptions: {
        controls: false
      }
    }
  }
}
</script>

<style>
.vimeo-example {
  max-width: 450px;
  margin: 2em auto;
}
.vimeo-example__embed {
  position: relative;
  /* 56% is the height of the video, relative to its width: don't change! */
  padding: 56% 0 0 0;
}
.vimeo-example__embed iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
