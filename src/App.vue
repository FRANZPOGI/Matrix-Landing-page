<script lang="ts" setup>
  import { logo, mockups } from './assets';

  const icons = ['facebook', 'twitter', 'instagram'];
</script>

<template>
  <div mb-8 flex flex-col items-center gap-14>
    <header w="full max-xs sm:max-w-md md:max-w-lg lg:max-4xl xl:max-6xl" class="mx-auto h-20 flex">
      <img :src="logo" alt="" width="140" />
    </header>

    <main
      class="max-w-xs mx-auto | flex flex-col gap-8 | sm:max-w-md md:max-w-lg lg:(max-w-4xl grid grid-cols-2 gap-12) xl:max-w-6xl"
    >
      <img :src="mockups" alt="" />
      <div flex flex-col items-center gap-6 text-center lg="items-start text-left">
        <h1 text-3xl font-poppins font-semibold lg="text-5xl leading-normal">
          BONUS LIFE
        </h1>
        <p md:text-lg leading-relaxed>
          Join my course and escape the matrix for just $2400. 
        </p>
        <button
          class="py-3 px-18 max-w-[fit-content] | bg-white rounded-full text-violet font-poppins transition duration-200 easin-in hover:(bg-magenta text-white shadow-md)"
        >
          Register
        </button>
      </div>
    </main>

    <footer class="lg:(w-full flex justify-end)">
      <ul flex gap-4 text-lg>
        <template v-for="icon in icons">
          <li
            class="h-9 min-w-9 w-9 | flex items-center justify-center | border-2 border-white rounded-full hover:(text-magenta border-magenta) transition duration-200 ease-in"
          >
            <button h-full w-full>
              <span sr-only> Follow us on {{ icon }} </span>
              <i :class="`bx bxl-${icon}`" />
            </button>
          </li>
        </template>
      </ul>
    </footer>
  </div>
</template>

<style>
  body {
    background-image: url(./assets/bg-mobile.svg);
    background-repeat: no-repeat;
  }

  @media screen and (min-width: 376px) {
    body {
      background-image: url(./assets/ivanedep.JPG);
      background-attachment: fixed;
      background-size: cover;
      background-position: center;
    }
  }
</style>
