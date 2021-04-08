<template>
  <div id="app" class="flex">
    <div class="w-2/5 p-10">
      <div class="mb-10">
        <ImageProfile class="mb-3"></ImageProfile>
        <Title big>Juan Pablo Müller</Title>
        <p>Software Engineer</p>
      </div>
      <div class="mb-10">
        <rounded-icon icon="user"></rounded-icon>
        <Title>Data & contact</Title>
        <data-contact :data_contact="data_contact"></data-contact>
      </div>
      <div>
        <rounded-icon icon="code"></rounded-icon>
        <Title>Skills</Title>
        <professional-skills :skills="professional_skills"></professional-skills>
      </div>
    </div>
    <div class="w-3/5 p-10">
      <div class="mb-10">
        <rounded-icon icon="glasses"></rounded-icon>
        <Title>Experience</Title>
        <professional-experience :experience="experience"></professional-experience>
      </div>
      <div class="mb-10">
        <rounded-icon icon="suitcase"></rounded-icon>
        <Title>Projects</Title>
        <projects :projects="projects"></projects>
      </div>
    </div>
  </div>
</template>

<script>
import ImageProfile from "@/components/ImageProfile";
import Title from "@/components/Title";
import RoundedIcon from "@/components/RoundedIcon";
import DataContact from "@/components/DataContact";
import ProfessionalSkills from "@/components/ProfessionalSkills";
import ProfessionalExperience from "@/components/ProfessionalExperience";
import Projects from "@/components/Projects";
export default {
  name: 'App',
  components: {
    Projects,
    ProfessionalExperience,
    ProfessionalSkills,
    DataContact,
    RoundedIcon,
    ImageProfile,
    Title
  },
  data:() => ({
    data_contact:{
      'Name': 'Juan Pablo Müller',
      'Age': 29,
      'e-mail': 'colomuller91@gmail.com',
      'Phone': '+54 9 3445 441341',
      'LinkedIn': '@colomu'
    },
    skill_level_base: 5,
    professional_skills:{
      'PHP':{
        skill_level:5,
        frameworks:['Laravel', 'SmartyPHP'],
      },
      'Javascript':{
        skill_level:3,
        frameworks:['Vue.js', 'NodeJS'],
      },
      'Pascal':{
        skill_level:3,
        frameworks:['Delphi']
      },
      'Integration':{
        skill_level:3,
        frameworks:['GIT','SVN']
      },
      'OS':{
        skill_level:4,
        frameworks:['Linux','Windows']
      },
      'Database':{
        skill_level:4,
        frameworks:['PostgreSQL','MySql','SAP Hana','SQL Server','IndexedDB']
      },
      'APIs':{
        skill_level:4,
        frameworks:['REST','SOAP']
      },
      'Others':{
        frameworks:['HTML', 'CSS', 'C#']
      }
    },
    experience:[
      {
        title:'Fullstack Developer',
        company:'Agrofina S.A.',
        from:'2016 September',
        to:'Actually',
        jobDescription:`Development of a desktop application on Delphi framework that fully manages the operations of the company (logistics, commercial, processes, wms, recipes, averages, reporting, etc.), rewrite modules from legacy system to new technologies like Laravel in order to modernize the application. On the other hand, develop and maintain an interface that integrates SAP with our system as well as a monitoring panel. Technologies that I use: PHP, Javascript, JQuery, Postgresql, Dephi, Bash script.`
      },
      {
        title:'Fullstack Developer',
        company:'Waitry',
        from:'2020 July',
        to:'Actually',
        jobDescription:`Waitry is a gastronomic management platform aimed at improving the customer's purchasing process. My main function it's development API integrations of our platform with POS systems and digital delivery services. In the same way, I participate developing functionalities in both frontend and backend. We mainly use our own framework developed in PHP, and Angular.js, MySQL, Laravel, Laravel Nova, Vue.js`
      },
      {
        title:'Fullstack Developer',
        company:'Cristal Media',
        from:'2020 July',
        to:'Actually',
        jobDescription:`Multiple projects`
      }
    ],
    projects:[
      {
        title:'Auction management',
        description:'Software de escritorio para gestión de remates, inventarios, liquidaciones y reportes'
      },
      {
        title:'Clinic hístory software',
        description:'WebApp para gestión de turnos, pacientes, fichas médicas, reporte de estadísticas y liquidación de coberturas médicas'
      },
      {
        title:'Websites',
        linkList:[
            '<a href="http://norteapp.com">norteapp.com</a>',
            '<a href="http://serka.com.ar">serka.com.ar</a>',
            '<a href="http://ocindumentaria.com.ar">ocindumentaria.com.ar</a>',
            '<a href="http://maryalquila.com">maryalquila.com</a>',
            '<a href="http://sitonegocios.com">sitonegocios.com</a>',
            '<a href="http://inmobiliariacarelli.com.ar">inmobiliariacarelli.com.ar</a>',
        ]
      }

    ]
  }),

}
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 1000px;
  margin: 0 auto;
}
</style>
