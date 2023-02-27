<template>
  <b-row style="margin-left: 0; margin-right: 0">
    <b-col md="4">
      <b-img
        src="../assets/hossein.webp"
        id="avatar-img"
        alt="Itsuka"
      />
    </b-col>

    <b-col md="8">
      <h2 class="intro animate__animated animate__fadeInUp animate__fast">
        Hi!,
        <br />I<span>'m Hossein</span>.
      </h2>

      <div class="col-md-10 info">
        My name is Hossein Boustani, I am a <b>DotNet Full-stack Developer</b>.
        <br />
        <b-button
          class="action-btn animate__animated animate__wobble animate__delay-4s animate__fast"
          to="/about"
        >
          Explore >
        </b-button>

        <!-- .SOCIAL LINKS SECTION -->
        <div
          class="social-icons animate__animated animate__fadeInUp animate__delay-1s"
        >
          <social-link :to="socialLinks.github">
            <GithubIcon />
          </social-link>

          <social-link :to="socialLinks.youtube">
            <YoutubeIcon />
          </social-link>

          <social-link :to="socialLinks.twitter">
            <TwitterIcon />
          </social-link>

          <social-link :to="socialLinks.telegram">
            <IosSend />
          </social-link>

          <social-link :to="socialLinks.linkedin">
            <LinkedinIcon />
          </social-link>
        </div>
      </div>
    </b-col>
  </b-row>
</template>

<script>
import GithubIcon from "vue-ionicons/dist/logo-github.vue";
import LinkedinIcon from "vue-ionicons/dist/logo-linkedin.vue";
import TwitterIcon from "vue-ionicons/dist/logo-twitter.vue";
import IosSend from "vue-ionicons/dist/ios-send.vue";
import FacebookIcon from "vue-ionicons/dist/logo-facebook.vue";
import YoutubeIcon from "vue-ionicons/dist/logo-youtube.vue";
import MailIcon from "vue-ionicons/dist/md-mail.vue";

export default {
  components: {
    GithubIcon,
    LinkedinIcon,
    TwitterIcon,
    IosSend,
    FacebookIcon,
    YoutubeIcon,
    MailIcon,
  },

  data() {
    return {
      avatar: require("@/assets/avatar-1.webp"),
      // ADD YOUR SOCIAL LINKS HERE 👇
      socialLinks: {
        github: "https://github.com/engboustani",
        youtube: "https://youtube.com/@HosseinBoustani",
        twitter: "https://twitter.com/engboustani",
        telegram: "https://t.me/engBoustani",
        linkedin: "https://www.linkedin.com/in/engboustani"
      },
    };
  },

  head: {
    title: "Hossein Boustani",
    meta: [
      {
        hid: "description",
        name: "description",
        content:
          "A Lightweight and Stable Discord Music Bot For Your Daily Production.",
      },
      {
        hid: "og:title",
        name: "og:title",
        content: "Hossein Boustani",
      },
      {
        property: "og:description",
        content:
          "A Lightweight and Stable Discord Music Bot For Your Daily Production.",
      },
      {
        hid: "og:image",
        name: "og:image",
        content: "../assets/hossein.PNG",
      },
    ],
  },
  mounted() {
    this.$nextTick(() => {
      this.$nuxt.$loading.start();

      setTimeout(() => this.$nuxt.$loading.finish(), 500);
    });
  },
};
</script>
