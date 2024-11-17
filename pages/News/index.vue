<template>
    <div class="news__page">
        <div class="page__header">
            <div class="bg">
                <img src="../../assets/images/hero-bg.png" alt="news page bg">
                <div class="bg__gradient"></div>
            </div>

            <div class="container">
                <h1>News</h1>
                <p>Recent press releases, company updates, and stakeholder news.</p>
                <NuxtLink to="Contact">
                    <button class="mt-4">CONTACT US</button>
                </NuxtLink>
            </div>
        </div>
        
        <section class="news__items">
            <div class="container">
                <NewsItem />
                <NewsItem />
                <NewsItem />
            </div>
        </section>
    </div>
</template>
<script>
export default {
    
}
</script>
<style lang="">
    
</style>