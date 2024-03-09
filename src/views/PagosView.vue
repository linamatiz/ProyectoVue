<template>
    <div>
      
      <h1> Pasarela de Pago</h1>
      <div v-if="!paymentComplete">
        <form @submit.prevent="processPayment">
          <!-- Campos de entrada de la información del usuario -->
          <div class="pagos">
          <input type="text"  v-model="cardNumber" placeholder="Número de Tarjeta">
          <br>
          <input type="text"  v-model="expDate" placeholder="Fecha de Expiración">
          <br>
          <input type="text" v-model="cvv" placeholder="CVV">
          <br>
          <button class ="botonpagar" type="submit">Pagar</button>
          </div>
        </form>
      </div>
      <div v-else>
       <strong>listo tu pago, revisa tu correo .</strong>
      </div>
    </div>
  </template>
  
  <script>
  
  export default {
  data() {
    return {
      cardNumber: '',
      expDate: '',
      cvc: '',
      paymentComplete: false
    };
  },
  methods: {
    processPayment() {
      // Simulación del proceso de pago
      setTimeout(() => {
        this.paymentComplete = true;
        alert("Pago completado. Gracias por tu compra.");
      }, 2000);
      //barra carga
      
    }
  }
};
//barra carga

</script>

  
  <style scoped>
  /* Estilos CSS para la vista */
  .paymentcomplete{
    background-color: #ffffff;
  padding: 20px;
  border-radius: 5px;
  text-align: center;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);

  }

  .pagos
  {
    
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    background-color: #637878;
    padding: 20px;
  }
  .botonpagar{
    border-radius: 8px; /* Bordes redondeados */
    background-color: #43d5e8; /* Cambia el color de fondo al pasar el cursor */
  }
  

    
  
  </style>
  