<template>
  <div>
    <nav :class="navIsOpen ? 'opened' : ''">
      <div class="container-lg container-fluid d-flex justify-content-between">
        <div class="left__nav">
          <img src="../assets/images/logo.svg" class="nav__logo" alt="logo" />
        </div>
        <div class="mid__nav">
            <NuxtLink
                :to="{ name: 'index' }"
                class="nav__link"
                :class="isRoute('index') ? 'active' : ''"
                >Home</NuxtLink
            >
            <NuxtLink
                :to="{ name: 'AboutUs' }"
                class="nav__link"
                :class="isRoute('AboutUs') ? 'active' : ''"
                >About Us</NuxtLink
            >
            <NuxtLink
                :to="{ name: 'News' }"
                class="nav__link"
                :class="isRoute('News') ? 'active' : ''"
                >News</NuxtLink
            >
            <NuxtLink
                :to="{ name: 'Contact' }"
                class="nav__link"
                :class="isRoute('Contact') ? 'active' : ''"
                >Contact</NuxtLink
            >
        </div>
        <div class="right__nav">
          <button class="me-5">JOIN THE FAMILY</button>
        </div>

        <div class="menu" @click.prevent="toggleNav">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="24"
            height="24"
            fill="currentColor"
            class="bi bi-list"
            viewBox="0 0 16 16"
            v-if="!navIsOpen"
          >
            <path
              fill-rule="evenodd"
              d="M2.5 12a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5m0-4a.5.5 0 0 1 .5-.5h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5"
            />
          </svg>
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="20"
            height="20"
            fill="currentColor"
            class="bi bi-x-lg"
            viewBox="0 0 16 16"
            v-else
          >
            <path
              d="M2.146 2.854a.5.5 0 1 1 .708-.708L8 7.293l5.146-5.147a.5.5 0 0 1 .708.708L8.707 8l5.147 5.146a.5.5 0 0 1-.708.708L8 8.707l-5.146 5.147a.5.5 0 0 1-.708-.708L7.293 8z"
            />
          </svg>
        </div>
      </div>
    </nav>
    <aside :class="navIsOpen ? 'show' : ''">
      <div>
        <NuxtLink
          :to="{ name: 'index' }"
          class="aside__link"
          :class="isRoute('index') ? 'active' : ''"
          @click.prevent="toggleNav"
          >Home</NuxtLink
        >
        <NuxtLink
          :to="{ name: 'AboutUs' }"
          class="aside__link"
          :class="isRoute('AboutUs') ? 'active' : ''"
          @click.prevent="toggleNav"
          >About Us</NuxtLink
        >
        <NuxtLink
          :to="{ name: 'News' }"
          class="aside__link"
          :class="isRoute('News') ? 'active' : ''"
          @click.prevent="toggleNav"
          >News</NuxtLink
        >
        <NuxtLink
          :to="{ name: 'Contact' }"
          class="aside__link"
          :class="isRoute('Conact') ? 'active' : ''"
          @click.prevent="toggleNav"
          >Contact</NuxtLink
        >
      </div>
      <div>
        <button>JOIN THE FAMILY</button>
      </div>
    </aside>
  </div>
</template>
<script setup>
import { ref, onMounted } from "vue";

const route = useRoute();
const navIsOpen = ref(false);

const toggleNav = () => {
  navIsOpen.value = !navIsOpen.value;
};

const isRoute = (current) => {
  return current === route.name;
};
</script>
