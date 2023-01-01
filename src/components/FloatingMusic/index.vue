<template>
  <div class="">
    <audio
      id="myAudio"
      src="../../../public/assets/music/Prep.mp3"
      class="hide"
      allow="autoplay"
      autoplay="true"
      loop
    ></audio>
    <img
      src="../../../public/assets/icons/music-icon.png"
      ref="music"
      alt=""
      id="icon-music"
      class=""
      @click="toggleMusic()"
    />
  </div>
</template>

<script>
import './css/main.scss';

export default {
  data() {
    return {
      isPlaying: false,
      myAudio: document.getElementById('myAudio'),
    };
  },
  methods: {
    toggleMusic() {
      let myAudio = document.getElementById('myAudio');
      if (this.isPlaying == false) {
        myAudio.play();
        this.isPlaying = true;
      } else {
        myAudio.pause();
        this.isPlaying = false;
      }
      console.log(this.isPlaying);
    },
  },
  // mounted() {
  //   this.$refs.music.click();
  // },
};
</script>
