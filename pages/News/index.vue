<template>
    <div class="news__page">
        <div class="page__header">
            <div class="bg">
                <video autoplay muted loop class="hero__video">
                    <source src="../../assets/videos/bg.mp4" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
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