<template>
  <section id="jobs" class="container std">
    <h2> Jobs </h2>
    <JobBox v-for="(job, key) in jobs" :key="key" :jt="job.title" :jd="job.description" />
    <p id="job-guide">mail to <strong>job@lovefrominc.com</strong> for applying</p>
  </section>
</template>

<script>
// @ is an alias to /src
import JobBox from "@/components/JobBox.vue";

export default {
  name: "jobs",
  components: {
    JobBox
  },
  data() {
    return{
      jobs: [
        { title: 'Assistant - US', description: 'We are looking for a personal assistant to work closely with Jony Ive and primarily manage his schedule. Individual salary setting.'},
        { title: 'Brand Identity Developer - US', description: 'We are looking for a brand identity developer that will build a postive reputation of LoveFrom both homeland and abroad. Marketing. Individual salary setting'},
        { title: 'Creative Director - Remote', description: 'We are looking for creative directors who will be in charge of our online presence such as social medias. Individual salary setting.'},
        { title: 'Financial Analyst - Remote', description: 'We are looking for a financial analyst who will primarily focus on getting investors onboard. Individual salary setting.'},
        { title: 'Financial Director - US', description: 'We are looking for a financial director who will manage the finance of the companies. Experience in finance, taxes and business relations are necessary. Individual salary setting.'},
        { title: 'Legal Advisor - Remote', description: 'We are looking for a legal advisor with experience in law mainly in the United States but will work worldwide. Need to have the ability to write business agreements, investing certificates and understand copyright laws. Individual salary setting.'},
        { title: 'Web Developer - Remote', description: 'We are looking for a web developer with experience in HTML5, JavaScript and CSS. Individual salary setting.'},
        { title: 'Web Developer - Remote', description: 'We are looking for a web developer with experience in HTML5, JavaScript and CSS. Individual salary setting.'},
        { title: 'Intern - Remote', description: 'Would you like to become an intern at the greatest design firm in the world? Tell us why we would like to have you onboard. Unpaid internship.'},
      ]
    }
  }
};
</script>
<style>
  #job-guide{
    margin-top: 68px;
    font-size: 12px;
    text-align: center;
  }
  @media screen and (min-width: 768px){
    #job-guide{
        font-size: 24px;
    }
  }
</style>
