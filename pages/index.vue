<template>
  <header class="header">
    <h1>Piluginasan</h1>
    <p>A band of soundnauts</p>
  </header>
  <main class="index">
    <section class="articles">
      <ul>
        <li v-for="(article, key) in data" :key="key">
          <plgnsn-article 
            :src="article.cover"
            :type="article.type"
            :alt="article.alt" 
            :title="article.title" 
            :year="article.year"
            :description="article.description"
            :linksArray="article.links"
          />
        </li>
      </ul>
    </section>
  </main>
</template>

<script setup lang="ts">
  const  { data } = await useAsyncData('/', () => queryContent('/releases').sort({id: -1}).find());
</script>

<style scoped>

  .header {
    padding: 2em 3em 0 3em;
  }

  .index {
    padding: 3em;
  }

  .articles ul {
    display: grid;
    gap: 3em;
  }
</style>