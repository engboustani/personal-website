<template>
  <div class="container animate__animated animate__fadeIn">
    <div class="row">
      <div class="col-md-6">
        <div class="about">
          <h1 class="line-after">About Me</h1>
          <h4 class="mt-4">Hey 👋</h4>
          <p>
            My name is Hossein Boustani, I am a <b>DotNet Full-stack Developer</b>.
          </p>
          <p>
            Highly skilled and innovative software development professional with 8 years of hands-on experience in web application development.
            Focused and efficient learner with practical expertise in mobile apps and automated
            testing, seeking a full stack developer position with Tosan.
          </p>
          <h4 class="mt-5">Skills</h4>
          <p>Here is a list of my skills:</p>
          <div class="row animate__animated animate__fadeInUp">
            <div class="col">
              <ul style="list-style-type: circle">
                <li>C#</li>
                <li>DotNet</li>
                <li>Entity Framework</li>
                <li>ASP.NET</li>
              </ul>
            </div>
            <div class="col">
              <ul style="list-style-type: circle">
                <li>SQL Server</li>
                <li>Rest APIs</li>
                <li>Security</li>
                <li>SignalR</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <img
          src="../assets/hossein2.webp"
          alt="Hossein Boustani"
          class="abt-img"
        />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      startYear: 2021,
      currYear: new Date().getFullYear(),
      stacks: [
        {
          language: "HTML",
          experience: "3+ Years",
          variant: "secondary",
          breif: "lorem...",
        },
        {
          language: "CSS",
          experience: "3+ Years",
          variant: "primary",
          breif: "lorem...",
        },
        {
          language: "Javascript",
          experience: "2+ Years",
          variant: "warning",
          breif: "lorem...",
        },
        {
          language: "VUE.JS",
          experience: "2+ Years",
          variant: "success",
          breif: "lorem...",
        },
        {
          language: "Node.js",
          experience: "2+ Years",
          variant: "dark",
          breif: "lorem...",
        },
      ],
    };
  },
  head: {
    title: "About - Itsuka",
    meta: [
      {
        hid: "description",
        name: "description",
        // currYear - startYear
        content: `A Lightweight and Stable Discord Music Bot For Your Daily Production.`,
      },
    ],
  },
};
</script>
<style scoped>
.container {
  margin-top: 140px;
  text-align: left;
}
.line-after {
  overflow: hidden;
}
.line-after::after {
  content: "";
  display: inline-block;
  height: 0.5em;
  vertical-align: bottom;
  width: 100%;
  margin-right: -100%;
  margin-left: 10px;
  border-top: 2px solid rgb(211, 46, 46);
}
.abt-img {
  width: inherit;
  height: inherit;
  border-radius: 5px;
}
/* .abt-img:hover {
  animation: swing;
  animation-duration: 2s;
} */
</style>
