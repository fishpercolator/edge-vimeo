<template>
  <div class="container">
    <div class="card vimeo-example">
      <div class="card-image">
        <div class="vimeo-example__embed">
          <vimeo-player ref="player" :video-id="148751763" />
        </div>
      </div>
      <div class="card-content">
        <p>Blah</p>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style>
.vimeo-example {
  max-width: 450px;
  margin: 2em auto;
}
.vimeo-example__embed {
  position: relative;
  /* 75% is the height of the video, relative to its width: don't change! */
  padding: 75% 0 0 0;
}
.vimeo-example__embed iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
</style>
