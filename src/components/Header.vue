<template>
  <nav class="header">
    <div class="nav-header">
      <h1>Isabella Bertucci</h1>
      <div class="status">Available <span class="online"></span>
      </div>
    </div>
    <div class="social-links">
      <a href="https://www.behance.net/isabellabertucci" target="_blank" aria-label="Behance">
        <font-awesome-icon :icon="['fab', 'behance']" />
      </a>
      <a href="https://dribbble.com/ibertucci" target="_blank" aria-label="Dribbble">
        <font-awesome-icon :icon="['fab', 'dribbble']" />
      </a>
      <a href="https://github.com/isabellabertucci" aria-label="GitHub" target="_blank">
        <font-awesome-icon :icon="['fab', 'github']" />
      </a>
      <a href="https://www.linkedin.com/in/isabella-bertucci-8641521a3/" aria-label="LinkedIn" target="_blank">
        <font-awesome-icon :icon="['fab', 'linkedin-in']" />
      </a>
    </div>
  </nav>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome';
import { library } from '@fortawesome/fontawesome-svg-core';
import { faBehance, faDribbble, faGithub, faLinkedinIn } from '@fortawesome/free-brands-svg-icons';

library.add(faBehance, faDribbble, faGithub, faLinkedinIn);

export default {
  components: {
    FontAwesomeIcon
  }
};
</script>

<style scoped>
.header {
  background-color: var(--bg-color);
  border-bottom: 1px solid rgba(233, 201, 180, 0.4);
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1400px;
  width: 100%;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1400px;
  width: 100%;
  margin: 0 auto;
  padding: 1rem 2rem;
}

.nav-header {
  display: flex;
}

.status {
  background-color: var(--text-color);
  padding: 0.4rem 1rem;
  border-radius: 32px;
  color: var(--bg-color);
  margin-left: 1rem;
}

.online {
  display: inline-block;
  width: 8px;
  height: 8px;
  background-color: #2FC37C;
  border-radius: 50%;
  margin-left: 4px;
}

.social-links a {
  margin: 0 0.5rem;
  color: var(--text-color);
}

@media (max-width: 768px) {
.header{
  padding: 1rem;
  margin: 0;
}

  .nav-header {
    display: flex;
    width: 100%;
    justify-content: space-between;
    text-align: center;
  
  }


  .status {
    padding: 0.5rem 0.5rem;
    margin: 0rem 0;
    text-align: center;
  }

  .social-links {
    display: none;
  }
}
</style>
