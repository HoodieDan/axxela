<template>
  <div>
    <NuxtLayout>
      <AppHeader />
      <NuxtPage />
      <AppFooter />
    </NuxtLayout>
  </div>
</template>

<script lang="ts" setup>
import 'bootstrap/dist/css/bootstrap.min.css'

useHead({
  title: 'Axxela Mechanical',
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/logo.svg'
    }
  ]
})
</script>

<style lang="scss">
@use "~/styles/index.scss";
</style>