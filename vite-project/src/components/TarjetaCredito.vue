<template>
    <div id="app">
      <!-- Formulario -->
      <form>
        <div>
          <label>Título de la tarjeta: </label>
          <input v-model="tituloTarjeta" />
        </div>
  
        <div>
          <label>Chip SRC: </label>
          <input v-model="chipSrc" />
        </div>
  
        <div>
          <label>Número: </label>
          <input v-model="numeroTarjeta" />
        </div>
  
        <div>
          <label>Fecha de expiración: </label>
          <input v-model="fechaExpiracion" />
        </div>
  
        <div>
          <label>Propietario: </label>
          <input v-model="propietario" />
        </div>
  
        <div>
          <label>Tipo de tarjeta SRC: </label>
          <input v-model="tipoTarjetaSrc" />
        </div>
      </form>
  
      <!-- Tarjeta de crédito -->
      <div class="carnet">
        <h3>{{ tituloTarjeta }}</h3>
        <img width="40" :src="chipSrc" alt="Chip" />
        <div>
          <h2>{{ numeroTarjeta }}</h2>
          <span>Fecha Exp: <b>{{ fechaExpiracion }}</b></span>
        </div>
        <footer>
          <span>{{ propietario }}</span>
          <img :src="tipoTarjetaSrc" width="60" alt="Tipo de tarjeta" />
        </footer>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        // Estado inicial de las variables
        tituloTarjeta: 'Visa Classic Crédito',
        numeroTarjeta: '400 500 600 700',
        fechaExpiracion: '01/30',
        propietario: 'William Henry Gates III',
        chipSrc: '/chip.png',
        tipoTarjetaSrc: '/visa.png',
      };
    },
  };
  </script>
  
  <style scoped>
  /* Estilos copiados del template HTML original */
  .carnet {
    width: 400px;
    height: 230px;
    background: #1c1a1e;
    color: white;
    border-radius: 20px;
    padding: 20px;
    box-shadow: 0px 0px 10px 2px black;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
  
  h3 {
    font-size: 20px;
  }
  
  h2 {
    font-size: 30px;
    letter-spacing: 10px;
    margin-bottom: 15px;
    text-shadow: 0px 0px 1px gold;
    font-family: Times;
  }
  
  b {
    font-size: 16px;
  }
  
  footer {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;
    font-weight: bold;
    font-size: 18px;
    text-transform: uppercase;
    font-style: italic;
  }
  </style>
  