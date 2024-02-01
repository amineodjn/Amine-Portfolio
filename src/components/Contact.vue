<template>
  <section id="contact" class="contact bg-less-dark">
    <div class="wrapper contact_wrapper bottom-border">
      <div class="contact_text">
        <h2 class="contact_headline header-xl">Contact</h2>
        <p class="contact_description">
          I would love to hear about your project and how i could help.
          Please fill in the form, and I'll get back to you as soons as possible.
        </p>
      </div>
      <form class="contact_form" @submit.prevent="sendEmail" >
        <div class="contact_control">
          <label for="name" class="visually-hidden">Name</label>
          <input v-model="emailData.name" type="text" id="name" name="name" placeholder="Name" required />
        </div>
        <div class="contact_control">
          <label for="email" class="visually-hidden">Email</label>
          <input v-model="emailData.email" type="email" id="email" name="email" placeholder="Email" required />
        </div>
        <div class="contact_control">
          <label for="message" class="visually-hidden">Message</label>
          <textarea v-model="emailData.bodyText" id="message" name="message" cols="30" rows="3" placeholder="Message" required></textarea>
        </div>
        <div class="contact_control aling-right">
          <button type="submit">Send Message</button>
        </div>
      </form>
    </div>
    <img class="contact_rings" src="/images/pattern-rings.svg" alt="" width="530" height="129" />
  </section> 
</template>
<script setup>
import { ref } from 'vue';

const emailData= ref({
  name: "",
  email: "",
  bodyText: ""
});

const sendEmail = () => {
  fetch('https://uf2lellxze.execute-api.us-east-1.amazonaws.com/prod/sendemail', {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json'
    },
    body: JSON.stringify(emailData.value)
  })
  .then(response => {
    if (!response.ok) {
      throw new Error('Network response was not ok');
    }
    alert('Email sent!');
  })
  .catch(err => {
    alert('Error sending email');
  });
}
</script>