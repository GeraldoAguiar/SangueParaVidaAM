<template>
  <div id="app">
    <Header-main />
    <section id="home" class="hero">
        <div class="hero-content">
          <div class="hero-shadow">
            <h1>Doe Sangue</h1>
            <p>Salvar vidas está ao nosso alcance!</p>
          </div>
        </div>
    </section>
    <main>
      <section id="Por_que_Doar_Sangue">
        <Recyclin-section />
      </section>

      <section id="Dicas_para_Doadores">
        <Coletivism-section />
      </section>
      <section id="Quem_Quando_e_Onde_pode_Doar">
        <Consientization-section />
      </section>
    </main>
    <Footer-main />
  </div>
</template>
<script>
import HeaderMain from "./components/header-main.vue";
import RecyclinSection from "./components/why-donate-blood-section.vue";
import ColetivismSection from "./components/tips-donors-section.vue";
import ConsientizationSection from "./components/who-when-where-donate-blood-section.vue";
import FooterMain from "./components/footer-main.vue";

export default {
  name: "App",
  components: {
    HeaderMain,
    RecyclinSection,
    ColetivismSection,
    ConsientizationSection,
    FooterMain,
  },
};
</script>

<style>
* {
  list-style-type: none;
}

ul{
  padding: 0;
  margin: 0;
}
ul li{
    padding: 0;
  margin: 0;
}
body,
html {
  margin: 0;
  padding: 0;
  font-family: "Roboto", sans-serif;
  background-color: #f5f5f5;
  color: #333;
  scroll-behavior: smooth;
}

#app {
  text-align: center;
}

.hero {
  background-image: url("https://images.unsplash.com/photo-1615461066159-fea0960485d5?crop=entropy&cs=tinysrgb&fit=crop&fm=jpg&h=900&ixid=MnwxfDB8MXxyYW5kb218MHx8Ymxvb2R8fHx8fHwxNzE2NjU4NzQy&ixlib=rb-4.0.3&q=80&utm_campaign=api-credit&utm_medium=referral&utm_source=unsplash_source&w=1600");
  background-size: cover;
  background-position: center;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
}

.hero-content h1 {
  font-size: 4rem;
  margin: 0;

}

.hero-content p {
  font-size: 1.5rem;
  margin: 0;


}

.hero-shadow{
  padding: .5rem;
  border-radius: 5px;
  background-color: rgba(0, 0, 0, 0.342);
}

.cards {
  display: flex;
  justify-content: space-around;
  margin-top: 20px;
}

.card {
  background: #ffffff;
  border: 1px solid #ddd;
  border-radius: 8px;
  width: 30%;
  margin: 10px;
  text-align: center;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.card img {
  width: 100%;
  border-bottom: 1px solid #ddd;
  border-radius: 8px 8px 0 0;
}

.card p {
  padding: 10px;
}

.card a {
  display: block;
  padding: 10px;
  background: #00796b;
  color: white;
  text-decoration: none;
  border-radius: 0 0 8px 8px;
}

main {
  padding: 2rem;
}

section {
  margin: 2rem 0;
  padding: 2rem;
  background: white;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

h2 {
  color: #ca2525;
}
h3 {
  color: #ca2525;
}

@media (max-width: 768px) {
  .hero-content h1 {
    font-size: 2.5rem;
  }

  .hero-content p {
    font-size: 1rem;
  }

  section {
    margin: 1rem 0;
    padding: 1rem;
  }
  .cards {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }

  .card {
    width: 100%;
  }
}

@media (max-width: 480px) {
  nav ul {
    flex-direction: column;
  }

  nav ul li {
    margin: 0.5rem 0;
  }

  .hero-content h1 {
    font-size: 2rem;
  }

  .hero-content p {
    font-size: 0.875rem;
  }

  section {
    margin: 1rem 0;
    padding: 1rem;
  }
}
</style>
