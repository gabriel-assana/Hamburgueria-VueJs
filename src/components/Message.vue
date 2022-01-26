<template>
  <div class="message-container">
    <p>{{ handleMsg(this.msg) }}</p>
  </div>
</template>

<script>
  export default {
    name: "Message",
    data(){
      return{
        message: ""
      }
    },
    props: {
        msg: Number,
      },
      methods:{
        handleMsg(msg){
          console.log(this.msg)
            switch(msg){
              case 1 :
                return this.message = "Pedido realizado com sucesso!"
              break;
              case 2 :
               return this.message = ""
              break;
              case 3 :
               return this.message = ""
              break;
            }
            
        },

      }
  }

</script>

<style scoped>
  .message-container {
    color: #004085;
    background-color: #cce5ff;
    border: 2px solid #b8daff;
    border-radius: 5px;
    padding: 10px;
    max-width: 400px;
    margin: 30px auto;
  }
</style>