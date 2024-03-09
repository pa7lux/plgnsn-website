<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
useHead({
  title: 'Piluginasan — Band of saundnauts',
  meta: [
    {
      name: 'description',
      content: 'Piluginasan is a band of saundnauts. We are a group of people who are passionate about sound and music. We are a collective of artists, musicians, and sound designers who are dedicated to creating and sharing music and sound art.'
    },
    {
      name: 'viewport',
      content: 'width=device-width, initial-scale=1.0'
    }
  ],
  link: [
    {
      rel: 'preconnect',
      href: 'https://fonts.googleapis.com',
    },
    {
      rel: 'preconnect',
      href: 'https://fonts.gstatic.com',
    },
    {
      rel: 'stylesheet',
      href: 'https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap',
    },
    {
      rel: 'shortcut icon',
      type: 'image/png',
      href: '/favicon.png',
    }
  ]
})
</script>

<style>
  *, *::before, *::after {
    box-sizing: border-box;
  }
  body {
    margin: 0;
    padding: 0;
    background-color: #fcfcfc;
    font-family: "Inter", sans-serif;
    font-optical-sizing: auto;
    font-weight: 300;
    font-style: normal;
    font-variation-settings:
    "slnt" 0;
    max-width: 1500px;
    margin: 0 auto;
    min-width: 360px;
    font-size: 22px;
  }

  @media (width <= 1400px) {
    body {
      font-size: 18px;
    }
  }

  @media (width <= 1200px) {
    body {
      font-size: 16px;
    }
  }

  h1, h2, h3, h4, h5, h6 {
    margin: 0;
  }
  
  img {
    width: 100%;
  }


  p {
    margin: 0;
  }

  ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  li {
    margin: 0;
    padding: 0;
  }

  a {
    text-decoration: none;
    color: inherit;
    display: inline-block;
    position: relative;
  }

  a::after {
    content: "";
    display: block;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 1px;
    background-color: currentColor;
    transform: translateY(100%) scaleX(.3);
    transform-origin: bottom left;
    transition: transform .3s ease-in-out;

  }

  a:hover::after {
    transform: translateY(100%) scaleX(1);
  }

  a:hover {
    opacity: 0.7;
  }
</style>
