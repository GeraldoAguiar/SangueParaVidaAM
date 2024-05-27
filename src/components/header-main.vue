<template>
  <header>
    <nav>
      <div class="menu-toggle" @click="toggleMenu">&#9776;</div>
      <ul :class="{ show: isMenuOpen }">
        <li><a href="#home" @click="toggleMenu">Home</a></li>
        <li><a href="#Por_que_Doar_Sangue" @click="toggleMenu">Porque Doar Sangue ?</a></li>
        <li><a href="#Dicas_para_Doadores" @click="toggleMenu">Dicas para Doadores</a></li>
        <li><a href="#Quem_Quando_e_Onde_pode_Doar" @click="toggleMenu">Quem, Quando e Onde pode Doar ?</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isMenuOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    }
  }
};
</script>

<style>
header {
  background: #d1423d;
  color: rgb(245, 240, 240);
  padding: 1rem 0;
  position: fixed;
  width: 100%;
  height: 40px;
  top: 0;
  z-index: 1000;
  display: flex;
  align-items: center;
  justify-content: center;
}

nav ul {
  list-style: none;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  padding: 0;
}

nav ul li {
  margin: 0 1rem;
}

nav ul li a {
  color: rgb(255, 255, 255);
  text-decoration: none;
  font-weight: 700;
}

nav ul li a:hover {
  text-decoration: underline;
}

@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    background: #2e7d32;
    position: absolute;
    width: 100%;
    top: 40px;
    left: 0;
    display: none;
  }
  
  nav ul li {
    margin: 1rem 0;
  }

  nav ul.show {
    display: flex;
  }
}

nav .menu-toggle {
  display: none;
}

@media (max-width: 768px) {
  nav .menu-toggle {
    display: block;
    position: absolute;
    top: 15px;
    right: 15px;
    font-size: 1.5rem;
    cursor: pointer;
  }
}
</style>
