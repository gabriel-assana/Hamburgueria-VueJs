<template>
  <div class="message-container">
    <p>{{ handleMsg(this.msg, this.idBurger) }}</p>
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
        idBurger: Number
      },
      methods:{
        handleMsg(msg, idBurger){
          console.log(this.idBurger)
          console.log(this.msg)
            switch(msg){
              case 1 :
                return this.message = "Pedido realizado com sucesso!"
              break;
              case 2 :
               return this.message = `Pedido de numero ${idBurger} esta em produção`
              break;
              case 3 :
               return this.message = `Pedido de numero ${idBurger} foi finalizado`
              break;
              case 4 :
               return this.message = `Pedido de numero ${idBurger} esta como solicitado`
              break;
              case 5 :
               return this.message = `Pedido de numero ${idBurger} foi cancelado`
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