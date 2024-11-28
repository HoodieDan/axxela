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
  ],
  meta: [
    { name: "description", content: `Axxela Mechanical (Axxela) provides mission-critical heating, ventilation, air conditioning and refrigeration (HVACR) services to Commercial and Industrial clients across Canada.  
                                    Axxela was formed to provide a better alternative for HVACR contractors looking to sell their business.  We know it takes decades not years to build a successful business so work diligently to preserve your company’s legacy and scale it to greater heights.  
                                    Our tailored and decentralized approach provides access to shared resources and support services so our partners and employees can focus on what they love most —providing top-notch service.` },
    { property: "og:title", content: 'Axxela Mechanical' },
    { property: "og:description", content: `Axxela Mechanical (Axxela) provides mission-critical heating, ventilation, air conditioning and refrigeration (HVACR) services to Commercial and Industrial clients across Canada.  
                                            Axxela was formed to provide a better alternative for HVACR contractors looking to sell their business.  We know it takes decades not years to build a successful business so work diligently to preserve your company’s legacy and scale it to greater heights.  
                                            Our tailored and decentralized approach provides access to shared resources and support services so our partners and employees can focus on what they love most —providing top-notch service.` },
    { property: "og:image", content: 'https://axxela.vercel.app/_nuxt/logo.BnaT1Sd1.svg' },
    { property: "og:url", content: `https://www.axxelamech.ca` }
  ]
})
</script>

<style lang="scss">
@use "~/styles/index.scss";
</style>