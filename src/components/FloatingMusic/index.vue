<template>
  <div class="">
    <audio
      id="myAudio"
      src="../../../public/assets/music/Prep.mp3"
      class="hide"
      loop
    ></audio>
    <img
      src="../../../public/assets/icons/music-icon.png"
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
  methods: {},
  computed: {
    toggleMusic() {
      //   let myAudio = document.getElementById('myAudio');
      //   if (isActive) {
      //     myAudio.play();
      //   } else {
      //     myAudio.pause();
      //   }
    },
  },
};
</script>
