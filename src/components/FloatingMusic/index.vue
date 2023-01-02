<template>
  <div class="">
    <audio
      src="../../../public/assets/music/Prep.mp3"
      id="myAudio"
      ref="audio"
      class="hide"
      allow="autoplay"
      autoplay="true"
      type="audio/mpeg"
      loop
    ></audio>
    <img
      src="../../../public/assets/icons/music-icon.png"
      ref="music"
      alt=""
      id="icon-music"
      class=""
      v-on:click="toggleMusic"
    />
  </div>
</template>

<script lang="ts">
import './css/main.scss';
import { defineComponent, onMounted, ref } from 'vue';

export default defineComponent({
  name: 'CommunicateVoice',
  data() {
    return {
      isPlaying: false,
      myAudio: document.getElementById('myAudio'),
    };
  },
  setup() {
    const audio = ref<HTMLAudioElement>();
    onMounted(() => {
      console.log(audio);
      //@ts-ignore
      audio.value?.play();
    });
    return {
      audio,
    };
  },
  methods: {
    toggleMusic() {
      this.isPlaying = !this.isPlaying;
      if (this.isPlaying) {
        this.audio.play();
      } else {
        this.audio.pause();
      }
    },
  },
});
// yang bisa
// export default {
//   data() {
//     return {
//       isPlaying: false,
//       myAudio: document.getElementById('myAudio'),
//     };
//   },
//   methods: {
//     toggleMusic() {
//       let myAudio = document.getElementById('myAudio');
//       if (this.isPlaying == false) {
//         myAudio.play();
//         this.isPlaying = true;
//       } else {
//         myAudio.pause();
//         this.isPlaying = false;
//       }
//       console.log(this.isPlaying);
//     },
//   },
// };
</script>
