<template>
    <div class="contact__page">
        <div class="page__header">
            <div class="bg">
                <video autoplay muted loop playsinline class="hero__video">
                    <source src="../assets/videos/bg.mp4" type="video/mp4" />
                    Your browser does not support the video tag.
                </video>
                <div class="bg__gradient"></div>
            </div>

            <div class="container">
                <h1>Contact Us</h1>
                <p>To get started, learn more about partnership oppurtunities, or for general inquiries</p>
            </div>
        </div>

        <section class="contact__body">
            <div class="container">
                <h3>Want to speak with us?</h3>
                <h3>Fill out this form and we will be in touch as soon as possible</h3>

                <form action="/" class="row">
                    <div class="row">
                        <div class="col-lg-6 col-md-6 left d-flex flex-column justify-content-between">
                            <div class="row">
                                <div class="col-lg-6 col-md-6">
                                    <label for="first_name">First Name</label>
                                    <input type="text" placeholder="First name">
                                </div>
                                <div class="col-lg-6 col-md-6">
                                    <label for="last_name">Last Name</label>
                                    <input type="text" placeholder="Last name">
                                </div>
                            </div>
                            <div class="email">
                                <label for="email">Email</label>
                                <input type="email" placeholder="you@company.com">
                            </div>
                            <div class="row">
                                <div class="col-lg-6 col-md-6">
                                    <label for="company">Your Company</label>
                                    <input type="text" placeholder="Your Company">
                                </div>
                                <div class="col-lg-6 col-md-6">
                                    <label for="phone">Your Phone</label>
                                    <input type="text" placeholder="Your Phone">
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6 col-md-6 right">
                            <label for="message">Message</label>
                            <textarea name="message" id="message" rows="18+" placeholder="How can we achieve your goals?"></textarea>
                        </div>
                    </div>
                    <div class="row">
                        <div class="col-lg-6 col md-6 desktop"></div>
                        <div class="col-lg-6 col md-6">
                            <button>Send Message</button>
                        </div>
                    </div>
                </form>
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