<template>
  <footer class="footer">
    <div class="content ">
    <p class="feedback">Your feedback is welcome 👍🏼</p>
    <section class="info">
      <p>Isabella Bertucci </p>
      <p>Product Maker</p>
    </section>
    <section class="social">
      <p><a href="mailto:isabella.bertucci13@gmail.com">isabella.bertucci17@gmail.com</a></p>
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
    </section>
  </div>
  </footer>
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

.footer {
  display: flex;
  justify-content: center;
  width: 100%;
  padding: 2rem;
  background: var(--highlight-color);
}

.content{
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 1400px;
}


p, a{
  color: var(--bg-color);
}

.info {
  display: flex;
  flex-direction: column;
  text-align: center;
}

.info p {
  margin: 0.5rem 0;
}

.social {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.social-links {
  display: flex;
  gap: 1rem;
}

.social a {
  color: var(--bg-color);
  text-decoration: none;
}

.social a:hover {
  text-decoration: underline;
}


@media (max-width: 768px) {
  .footer {
    flex-direction: column; 
    align-items: start; 
    padding: 1rem;
  }
  .social{
    align-items: flex-end;
  }

  .social-links {
    align-items: start; 
    margin-top: 1rem; 
  }

  .social-links a {
    margin-bottom: 0.5rem;
  }

  .feedback{
    display: none;
  }
}
</style>
