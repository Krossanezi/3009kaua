<template>

    <!DOCTYPE html>
    <html lang="en">
    <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
     
    </head>
    <body>
      <section class="banner">
            <div class="texto">
               <h1 class="titulo"></h1>
               <h2 class="sub_titulo"></h2>
              <div class="botoes">
        <figure>
        </figure>
        <br>
                 <a href="sobre.html"> <button class="overlay">Bem vindo ao seu template</button></a> 
                 
                   <a href="parceiros.html"><button class="overlay">Aqui será mostrado um pouco da pandemia em forma de memes.</button> </a>
               </div>
            </div>
        </section>
    <br><br>
    <link rel="stylesheet" href="script.js">  
    
    
    
    <div class="fotos">
      <div class="image1">
    <img src= "@/assets/kaua.jpg"  width="300px">
      </div>
    <br>
<div class="image2">
    <img src= "@/assets/kaua2.jpg"  width="300px">
  </div>
  <br>
  <div class="image3">
    <img src= "@/assets/kaua3.jpg" width="300px">
  </div>
    <br>
    <div class="image4">
    <img src= "@/assets/kaua4.jpg" width="300px">
  </div>
</div>
<div class="skeleton" v-if="!loaded"></div>
<img :src="src" @load="loaded = true" v-else alt="Imagem">
<div>
    <img v-lazy="imageSrc" alt="Descrição da imagem" />
  </div>
    </body>
    </html>
        
    </template>
    
    <script>
     export default {
  props: ['src'],
  data() {
    return {
      loaded: false
    };
  }
}; 
    </script>
    
    <!-- Add "scoped" attribute to limit CSS to this component only -->
    <style scoped>
    h1{
      color:hwb(153 12% 66%);
    }
    h3 {
      margin: 40px 0 0;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      display: inline-block;
      margin: 0 10px;
    }
    a {
      color: hwb(153 12% 66%);
    }
    table {
        width: 100%;
        border-collapse: collapse;
    }
    th, td {
        border: 1px solid #dddddd;
        text-align: left;
        padding: 8px;
    }
    th {
        background-color: #f2f2f2;
    }
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600&display=swap');
    
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
        font-family: 'Poppins', sans-serif;
    }
    
    nav {
        background-color: #189d35;
        padding: 10px 50px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
    
    nav .logo a {
        text-decoration: none;
        color: white;
        font-size: 35px;
        font-weight: 600;
    }
    
    nav ul {
        display: flex;
        align-items: center;
        list-style: none;
        padding: 10px;
    }
    
    nav li {
        margin-left: 7px;
    }
    
    nav li a {
        text-decoration: none;
        color: #fff;
        font-size: 18px;
        font-weight: 500;
        padding: 8px 15px;
        border-radius: 5px;
        transition: 0.3s;
    }
    
    nav li a:hover {
        background-color: white;
        color: black;
    }
    .texto .botoes {
        margin-top: 1px;
    
    }
    
    .texto .botoes button {
        height: 90px;
        width: 170px;
        border-radius: 5px;
        border: 0;
        margin: 0 10px;
        font-size: 20px;
        font-weight: 500;
        padding: 0 10px;
        cursor: pointer;
        outline: none;
        transition: 0.3s;
    }
    
    .texto .botoes button.n-overlay {
        color: white;
        background: none;
        border: 2px solid white;
    }
    
    .texto .botoes button.n-overlay:hover {
        color: black;
        background-color: white;
    }
    
    .texto .botoes button.overlay {
        background: linear-gradient(rgba(30, 105, 0, 0.486),rgba(248, 0, 0, 0.493));
        color: white;
        animation: vibrar 0.5s ease-in-out infinite both;
    }
    
    @keyframes vibrar {
        0% {
            transform: scale(1);
        }
    
        50% {
            transform: scale(1.1);
        }
    
        100% {
            transform: scale(1);
        }
    }
    .pic{
      width: 300px
      
    }
  
    @keyframes vibrar {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.1);
    }
    100% {
        transform: scale(1);
    }
}

.fotos {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
    margin: 20px 0; /* Espaçamento entre as fotos e o restante */
}

.image-container {
    display: flex;
    justify-content: space-between;
    margin: 10px; /* Espaçamento entre as linhas de imagens */
}

img {
    margin: 10px; /* Espaçamento entre as imagens */
    border-radius: 8px; /* Estilo opcional */
}
.botoes {
  display: flex;
  justify-content: center; /* Alinha os botões ao centro */
  gap: 20px; /* Define um espaçamento entre os botões */
  margin-top: 20px; /* Adiciona espaço acima dos botões */
}
.skeleton {
  width: 300px;
  height: 200px;
  background: #eee;
}
    </style>
    