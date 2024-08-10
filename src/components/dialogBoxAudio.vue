<template>
  <div style="display: flex">
    <div class="boxStyleComponent4">
      <div style="display: flex">
        <img
          :src="iconPlay"
          style="width: 60px; height: 60px; cursor: pointer"
          @click="playAudio"
          v-if="this.showPlay === true"
        />
        <img
          :src="iconPause"
          style="width: 60px; height: 60px; cursor: pointer"
          @click="pauseAudio"
          v-else
        />
        <q-slider
          v-model="sliderValue"
          :min="0"
          :max="audioDuration"
          style="margin-top: 14px"
          @input="updateTime"
        />
        <div style="padding: 5px 0px 0px 10px">
          <img class="profileImg" :src="this.imageProfile" />
        </div>
      </div>
    </div>
    <div class="ponteiroUser"></div>
  </div>
</template>
<script>
import iconPlay from "@/assets/icon/play_arrow.svg";
import iconPause from "@/assets/icon/pause.png"; // eslint-disable-next-line
import { ref, onUnmounted } from "vue";

export default {
  props: {
    audioSrc: {
      type: String,
      required: true,
    },
    imageProfile: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      iconPlay,
      iconPause,
      showPlay: true,
      audio: null,
      sliderValue: 0,
      audioDuration: 0,
      intervalId: null,
    };
  },
  methods: {
    playAudio() {
      if (!this.audio) {
        this.audio = new Audio(this.audioSrc);
        this.audio.addEventListener("loadedmetadata", () => {
          this.audioDuration = this.audio.duration;
        });
        this.audio.addEventListener("timeupdate", () => {
          this.sliderValue = this.audio.currentTime;
        });
        this.audio.addEventListener("ended", () => {
          this.showPlay = true;
          this.sliderValue = 0;
        });
      }
      this.audio.play();
      this.showPlay = false;
      this.intervalId = setInterval(() => {
        if (this.audio) {
          this.sliderValue = this.audio.currentTime;
        }
      }, 1000);
    },
    pauseAudio() {
      if (this.audio) {
        this.audio.pause();
        clearInterval(this.intervalId);
        this.intervalId = null;
      }
      this.showPlay = true;
    },
    updateTime() {
      if (this.audio) {
        this.audio.currentTime = this.sliderValue;
      }
    },
  },
  watch: {
    audioSrc(newSrc) {
      if (this.audio) {
        this.audio.src = newSrc;
        this.audio.load();
      }
    },
  },
  onUnmounted() {
    if (this.audio) {
      this.audio.pause();
      clearInterval(this.intervalId);
    }
  },
};
</script>
<style>
.boxStyleComponent4 {
  width: 550px;
  min-height: 56px;
  padding: 30px 15px;
  border-radius: 20px 0px 20px 20px;
  background-color: #d9fdd3;
  text-align: center;
  color: #111b21;
  border: none;
}

@media only screen and (max-width: 600px) {
  .boxStyleComponent4 {
    width: 380px;
    min-height: 56px;
    padding: 30px 15px;
    border-radius: 20px 0px 20px 20px;
    background-color: #d9fdd3;
    text-align: center;
    color: #111b21;
    border: none;
  }
}
.ponteiroUser {
  background-color: #d9fdd3;
  border-radius: 0px 0px 400px 0px;
  width: 12px;
  height: 14px;
  border: none;
}

.profileImg {
  background-color: #111b21;
  width: 50px;
  height: 50px;
  border-radius: 50px;
  border: none;
}
</style>