<template>
    <div style="display: flex;">
        <div class="pointerUserLeft"></div>
        <div id="boxStyleComponentLeft">{{ displayedMessage }}</div>
    </div>
    <div class="q-pa-md row justify-center">
    <div style=" max-width: 500px; ">
      <q-chat-message
        label="Sunday, 19th"
      />

      <q-chat-message
        name="me"
        avatar="https://cdn.quasar.dev/img/avatar4.jpg"
        :text="[ displayedMessage ]"
        sent
        stamp="7 minutes ago"
      />
      <q-chat-message
        name="Jane"
        avatar="https://cdn.quasar.dev/img/avatar3.jpg"
        :text="['doing fine, how r you?']"
        stamp="4 minutes ago"
      />
    </div>
  </div>
</template>
<script>
export default {
 props: {
 },
 mounted() {
    this.typeMessage();
 },
  data() {
    return {
     message: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.",
     displayedMessage: "",
     count: 0,
     speed: 80,
    };
  },
  methods: {
    typeMessage(){
        if (this.count < this.message.length) {
            this.displayedMessage += this.message.charAt(this.count);
            this.count++;
            setTimeout(this.typeMessage, this.speed);
        }
      }
  }
}

</script>
<style>
#boxStyleComponentLeft{
    width: 50%;
    height: 256px;
    padding: 30px 15px;
    border-radius: 0px 20px 20px 20px ;
    background-color: #f4f4f4;
    text-align: center;
    color: #0b141a;
}

.pointerUserLeft{
    background-color: #f4f4f4;
    border-radius: 0px 0px 0px 400px ;
    width: 12px;
    height: 14px;
}
</style>