<template>
  <div style="display: flex"   >
    <div class="pointerUserLeft"></div>
    <div id="boxStyleComponentLeft2">{{ displayedMessage }}</div>
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
#boxStyleComponentLeft2 {
  width: 550px;
  min-height: 56px;
  padding: 30px 15px;
  border-radius: 0px 20px 20px 20px;
  background-color: #f4f4f4;
  font-size: 18px;
  text-align: center;
  color: #0b141a;
}

@media only screen and (max-width: 600px) {
  #boxStyleComponentLeft2 {
    width: 380px;
    min-height: 56px;
    padding: 30px 15px;
    border-radius: 0px 20px 20px 20px;
    background-color: #f4f4f4;
    text-align: center;
    color: #0b141a;
  }
}

.pointerUserLeft {
  background-color: #f4f4f4;
  border-radius: 0px 0px 0px 400px;
  width: 12px;
  height: 14px;
}


</style>