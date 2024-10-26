<template>

  <div id="app">
    <Header />
    <main>
      <Introduction />
      <Projects />
    </main>
  </div>
  <Footer />
</template>

<script>
import './styles/global.css';
import Header from './components/Header.vue';
import Introduction from './components/Introduction.vue';
import Projects from './components/Projects.vue';
import Footer from './components/Footer.vue';

export default {
  components: {
    Header,
    Introduction,
    Projects,
    Footer
  }
};
</script>


<style>
#app {
  font-family: 'Poppins', sans-serif;
 
}

main {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: 1400px;
  padding: 2rem  ;
  margin: 0 auto ;
}
</style>
