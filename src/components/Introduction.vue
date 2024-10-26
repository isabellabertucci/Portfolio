<template>
  <section class="hero">
    <section class="hero-content-wrapper">

      <div class="details-wrapper">
        <div class="introduction">
          <h2>👋🏻 Hi, I'm <span>Isabella </span> </h2>
        </div>

        <div class="description">
          <p>
            I'm a Front-end Developer with a background in <strong>UI/UX design</strong>, guiding projects from discovery to delivery,
            and aligning business goals with user needs.
          </p>
        </div>
        <div class="description-wrappper">
          <div>
            <p>
              🌱 I'm looking for new opportunities
            </p>
            <p>
              📍 Previously at <strong> Zapify</strong>
            </p>
          </div>
          <div>
            <p> Isabella Bertucci</p>
            <p>
              <a href="mailto:isabella.bertucci17@gmail.com"> isabella.bertucci17@gmail.com</a>
            </p>
          </div>
        </div>

        <div class="jobs">
          <p>With over 3 years of experience in <strong> UX/UI design 🎨✨</strong></p>
          <p>I've had the opportunity to work on diverse projects that blend creativity and functionality, always aiming
            to elevate user experiences 🤝.</p>
        </div>
        <p class="projects">
          👇🏻 Check out my last 3 projects
        </p>
      </div>
    </section>

    <div class="technology-illustration">
      <div class="card">
        <div class="img-wrapper">
          <img src="/images/techs.png" alt="">
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import '@/styles/global.css'
export default {
  name: 'Introduction'
};
</script>

<style scoped>
.hero {
  display: flex;
  padding-top: 2rem;
  padding-bottom: 2rem;
  justify-content: space-between;
  gap: 5rem;
}

.hero-content-wrapper {
  display: flex 1;
}

.hero-ilustration-wrapper {
  display: flex 1;
}

.details-wrapper {
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.description-wrappper {
  display: flex;
  flex: 1;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 2rem;
  color: var(--text-color);


  & div:nth-child(2) a {
    text-decoration: none;
    color: var(--highlight-color);

    &:hover {
      text-decoration: underline;
    }
  }
}


.introduction {
  flex: 1;
  text-align: start;
}

.introduction h2 {
  font-size: 2.5rem;
  color: var(--text-color);
}

p {
  font-size: 1.2rem;
}

.introduction p {
  color: var(--text-color);
  line-height: 1.6;
}

.description {
  max-width: 600px;
  color: var(--text-color);
  ;
}

.contact a {
  text-decoration: none;
}

span {
  color: var(--highlight-color);
}

.contact a:hover {
  text-decoration: underline;
}

.img {
  width: 40px;
  height: 40px;
}

.projects {
  font-size: calc(clamp(1.25rem, 0.39vw + 1.159rem, 1.5rem));
  margin-top: 4rem;
  margin-bottom: 2rem;
  font-weight: 600;
}
.technology-illustration{
  object-fit: cover;
}

@media (max-width: 1000px) {
  .hero {
    flex-direction: column-reverse;
    align-items: center;
    padding: 0;
    margin-top: 1rem;
    gap: 0;
  }

  .description-wrappper {
    gap: 0;
  }

  h2 {
    margin: 0;
  }

  .hero-content-wrapper {
    margin-top: 0;
  }

  .row {
    flex-direction: column;
    align-items: flex-start;
  }


}
</style>
