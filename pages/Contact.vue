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
        <p>To get started, learn more about partnership opportunities, or for general inquiries</p>
      </div>
    </div>

    <section class="contact__body">
      <div class="container">
        <h3>Want to speak with us?</h3>
        <h3>Fill out this form and we will be in touch as soon as possible</h3>

        <form @submit.prevent="sendEmail" class="row">
          <div class="row">
            <div class="col-lg-6 col-md-6 left d-flex flex-column justify-content-between">
              <div class="row">
                <div class="col-lg-6 col-md-6">
                  <label for="first_name">First Name</label>
                  <input
                    type="text"
                    id="first_name"
                    v-model="firstName"
                    placeholder="First name"
                    required
                  />
                </div>
                <div class="col-lg-6 col-md-6">
                  <label for="last_name">Last Name</label>
                  <input
                    type="text"
                    id="last_name"
                    v-model="lastName"
                    placeholder="Last name"
                    required
                  />
                </div>
              </div>
              <div class="email">
                <label for="email">Email</label>
                <input
                  type="email"
                  id="email"
                  v-model="email"
                  placeholder="you@company.com"
                  required
                />
              </div>
              <div class="row">
                <div class="col-lg-6 col-md-6">
                  <label for="company">Your Company</label>
                  <input
                    type="text"
                    id="company"
                    v-model="company"
                    placeholder="Your Company"
                  />
                </div>
                <div class="col-lg-6 col-md-6">
                  <label for="phone">Your Phone</label>
                  <input
                    type="text"
                    id="phone"
                    v-model="phone"
                    placeholder="Your Phone"
                  />
                </div>
              </div>
            </div>
            <div class="col-lg-6 col-md-6 right">
              <label for="message">Message</label>
              <textarea
                id="message"
                v-model="message"
                rows="6"
                placeholder="How can we achieve your goals?"
                required
              ></textarea>
            </div>
          </div>
          <div class="row mt-4">
            <div class="col-lg-6 col md-6"></div>
            <div class="col-lg-6 col md-6">
              <button type="submit">Send Message</button>
            </div>
          </div>
        </form>
      </div>
    </section>
  </div>
</template>

<script setup>
import { ref } from "vue";

const firstName = ref("");
const lastName = ref("");
const email = ref("");
const company = ref("");
const phone = ref("");
const message = ref("");

const sendEmail = () => {
  const recipient = "nate@axxelamech.ca";
  const subject = encodeURIComponent("Axxela Contact Request");
  const body = encodeURIComponent(
    `First Name: ${firstName.value}\n` +
      `Last Name: ${lastName.value}\n` +
      `Email: ${email.value}\n` +
      `Company: ${company.value}\n` +
      `Phone: ${phone.value}\n` +
      `\n` +
      `Message: ${message.value}`
  );

  const mailtoLink = `mailto:${recipient}?subject=${subject}&body=${body}`;
  window.location.href = mailtoLink;
};
</script>

<style scoped>
/* Add your styles here */
</style>
