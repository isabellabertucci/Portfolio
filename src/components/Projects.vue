<template>
  <section class="project-list">
    <div class="project" v-for="project in projects" :key="project.title">
      <router-link :to="project.link">
        <div class="img-container">
          <img :src="project.image" :alt="project.title" class="project-image" />
        </div>
        <p class="project-title">{{ project.title }}</p>
      </router-link>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        { title: 'Utizie APP', image: '/images/utizie.png', link: 'https://www.behance.net/gallery/172372523/Utizie-App' },
        { title: 'Motion Design Product Website', image: 'http://placehold.co/400', link: '/product-website' },
        { title: 'Whatever REST API', image: 'http://placehold.co/400', link: '/rest-api' }
      ]
    };
  }
};
</script>

<style scoped>
.project-list {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  gap: 4rem;
  justify-content: center;
  margin-bottom: 2rem;
  margin-left: 0;
}

.img-container {
  overflow: hidden;
  border-radius: 1rem;
  width: 400px;
  height: 300px;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: all 1s ease-in-out;
  aspect-ratio: 4/3;

  &:hover {
    transform: scale(1.1);
  }
}

.project-title {
  color: var(--text-color);
  margin-top: 1rem;
}

@media (max-width: 768px) {

  .project-list {
    flex-direction: column;
    align-items: start;
    gap: 1.5rem; 
    margin: 0;
  }

  .img-container {
    max-width: 300px; /* Limita a largura máxima */
    height: auto;
  }
}

</style>
