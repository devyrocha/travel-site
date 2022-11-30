<template>
  <div class="container">
    <header>
      <img class="img" :src="imgLogo" alt="" />
      {{ imgLogo }}
      <input-search />
      <h1>EXPLORE A NATUREZA</h1>
    </header>
    <main>
      <h3>Destino</h3>

      <div class="cards">
        <card v-for="item in cardData" :key="item" :listCard="item" />
      </div>
    </main>

    <footer>
      <h3>Saiba Mais</h3>

      <ul>
        <li><a href="https:/www.google.com"> Sobre a Empresa</a></li>
        <li>Perguntas Frequentes</li>
        <li>Trabalhe conosco</li>
        <li>Meios de pagamento</li>
        <li>Contato</li>
      </ul>
    </footer>
  </div>
</template>

<script>
import Card from "./components/card.vue";
import InputSearch from "./components/input-search.vue";
export default {
  name: "App",
  components: { InputSearch, Card },
  data() {
    return {
      imgLogo: "/img/background.jpg",

      cardData: [
        {
          destino: "Floresta",
          imageUrl: "/img/background.jpg",
          link: "https://www.viajali.com.br/florestas-mais-incriveis-do-mundo/",
        },
        {
          destino: "Praia ",
          imageUrl: "/img/1.jpg",
          link: "https://www.skyscanner.com.br/noticias/inspiracao/20-belas-praias-no-brasil",
        },
        {
          destino: "Montanha",
          imageUrl: "/img/2.jpg",
          link: "https://www.terramundi.com.br/blog/destinos-de-montanhas-em-fotos-e-dicas/",
        },
        {
          destino: "Centro Urbano",
          imageUrl: "/img/3.jpg",
          link: "https://www.guiaviagensbrasil.com/blog/category/destinos-urbanos/",
        },
      ],
    };
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

.container {
  padding: 10px;
  width: 100%;
  background: #f6f6f6;
}
.img {
  position: absolute;
  width: 97%;
  height: 80vh;
}
h1 {
  position: relative;
  color: #fff;
  font-size: 80px;
  width: 250px;
  top: 15rem;
  left: 3rem;
}
main {
  position: relative;
  margin-top: 22rem;
  padding: 20px;
  font-size: 28px;
  font-weight: lighter;
}

.cards {
  width: 100%;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  padding-top: 5rem;
  justify-items: center;
}

footer {
  width: 100%;
  height: auto;
  background: #222222;
  padding: 15px;
  border-radius: 10px;
  color: #fff;
}

footer h3 {
  padding: 10px;
  font-size: 30px;
}

ul {
  margin: 2% 5% 1% 5%;
  width: 100%;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 35px;
  padding: 15px;
  list-style-type: none;
}

li {
  font-weight: 300;
  font-size: 15px;
  cursor: pointer;
}

li a{
  text-decoration: none;
  color: #fff
}
</style>>
