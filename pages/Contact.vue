<template>
  <b-container class="page animate__animated animate__fadeIn">
    <b-row class="justify-content-center">
      <b-col cols="md-6">
        <h2>Get in touch 💌</h2>

        <p class="text-left">
          If you have any question or just want to say hi, i'll try my best to
          get back to you.
        </p>

        <contact-form></contact-form> 
      </b-col>
    </b-row>
  </b-container>
</template>
<script>

import ContactForm from '../components/ContactForm.vue';

export default {
  data() {
    return {
      showAlert: false,
      formData: {
        name: "",
        email: "",
        message: "",
      },
    };
  },
  methods: {
    async sendMessage(e) {
      const self = this;
      var data = new FormData();

      data.append("Name", self.formData.name);
      data.append("Email", self.formData.email);
      data.append("Message", self.formData.message);

      fetch("https://formspree.io/f/mvodbwva", {
        method: "POST",
        body: data,
        headers: {
          Accept: "application/json",
        },
      }).then((response) => {
        if (response.ok) {
          this.showAlert = true;
          form.reset();
        } else {
          alert("Sending message failed, please try again");
        }
      });
      // .catch(error => {
      //   alert("Sending message failed, please try again");
      // });
    },
  },
  head: {
    title: "Contact - Hossein Boustani",
    meta: [
      {
        hid: "description",
        name: "description",
        content: "If you have any question or just want to say hi, i'll try my best to get back to you.",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Contact - Hossein Boustani",
      },
      {
        property: "og:description",
        content: "If you have any question or just want to say hi, i'll try my best to get back to you.",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: require("@/assets/contact.jpg"),
      },
    ],
  },
  components: {ContactForm}
};
</script>
<style scoped>
.container {
  margin-top: 120px;
}
form {
  margin-top: 40px;
  text-align: left;
}
</style>
