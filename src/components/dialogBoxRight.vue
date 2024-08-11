<template>
  <div style="display: flex"  class="positionBox">
    <div class="boxStyleComponent1">{{ displayedMessage }}</div>
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
.boxStyleComponent1 {
  width: 550px;
  min-height: 56px;
  padding: 30px 15px;
  font-size: 18px;
  border-radius: 20px 0px 20px 20px;
  background-color: #d9fdd3;
  text-align: center;
  color: #111b21;
}

@media only screen and (max-width: 600px) {
  .boxStyleComponent1 {
    width: 380px;
    min-height: 56px;
    padding: 30px 15px;
    font-size: 18px;
    border-radius: 20px 0px 20px 20px;
    background-color: #d9fdd3;
    text-align: center;
    color: #111b21;
  }
}

.ponteiroUser {
  background-color: #d9fdd3;
  border-radius: 0px 0px 400px 0px;
  width: 12px;
  height: 14px;
}

.positionBox {
   padding: 0px 0px 0px 190px ;
}

@media only screen and (max-width: 600px) {
  .positionBox {
    padding: 0px 0px 0px 0px;
  }
}
</style>