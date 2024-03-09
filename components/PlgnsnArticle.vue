<template>
  <article>
    <div class="image">
      <img :src :alt>
    </div>
    <div class="description">
      <h2>{{ title }}</h2>
      <p class="type">{{ type }}</p>
      <p>{{ description }}</p>
    </div>
    <p class="year">{{ year }}</p>
    <ul class="links">
      <li v-for="(link, index) in linksArray">
        <a :href="link[Object.keys(link)[0]]" target="_blank">{{Object.keys(link)[0]}}</a>
      </li>
    </ul>
</article>
</template>

<script setup lang="ts">
defineProps({
  src: String,
  alt: String,
  title: String,
  description: String,
  type: String,
  linksArray: Array,
  year: String
})

</script>

<style scoped>
article {
  display: grid;
  grid-template-columns: 1fr 3fr;
  grid-template-rows: 1fr 1fr;
  gap: 0.5em 1em;
  align-items: self-end;
}

@media (width >= 1400px) {
  article {
    grid-template-columns: 3fr 4fr;
  }
}

@media (width <= 1400px) {
  article {
    grid-template-columns: 2fr 4fr;
  }
}

@media (width <= 1200px) {
  article {
    grid-template-columns: 2fr 3fr;
  }
}

@media (width <= 1000px) {
  article {
    grid-template-columns: 2fr 4fr;
  }
}

@media (width <= 850px) {
  article {
    grid-template-columns: 2fr 3fr;
  }
}

@media (width <= 750px) {
  article {
    grid-template-columns: 1fr 1fr;
  }
}

@media (width <= 700px) {
  article {
    grid-template-columns: 1fr;
  }
}

.description {
  align-self: start;
}

h2 {
  margin-bottom: .5em;
}

.type {
  font-weight: bold;
  margin-bottom: .5em;
}

.image {
  grid-row: 1/4;
  border-radius: 1em;
  overflow: hidden;
}

.image img {
  aspect-ratio: 1/1;
  object-fit: cover;
  width: 100%;
  object-position: center;
}

.year {
  font-weight: bold;
}

.links {
  display: flex;
  gap: 1em;
}
</style>