<template>
  <div style="display: flex">
    <div class="boxStyleComponent">{{ displayedMessage }}</div>
    <div class="ponteiroUser"></div>
  </div>
</template>
<script>
export default {
  props: {
    message: {
      type: String,
      required: true,
    },
  },
  mounted() {
    this.typeMessage();
  },
  data() {
    return {
      displayedMessage: "",
      count: 0,
      speed: 80,
    };
  },
  methods: {
    typeMessage() {
      if (this.count < this.message.length) {
        this.displayedMessage += this.message.charAt(this.count);
        this.count++;
        setTimeout(this.typeMessage, this.speed);
      }
    },
  },
};
</script>
<style>
.boxStyleComponent {
  width: 50%;
  height: 256px;
  padding: 30px 15px;
  border-radius: 20px 0px 20px 20px;
  background-color: #d9fdd3;
  text-align: center;
  color: #111b21;
}

.ponteiroUser {
  background-color: #d9fdd3;
  border-radius: 0px 0px 400px 0px;
  width: 12px;
  height: 14px;
}
</style>