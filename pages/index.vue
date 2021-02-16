<template>
  <div class="mx-auto max-w-7xl p-5">
    <div class="flex items-center pb-5">
      <div class="px-10">
        <img class="h-32" src="~/assets/portrait.svg"/>
      </div>
      <div>
        <div class="md:flex justify-between items-center">
          <div class="space-y-4">
            <h1 class="text-5xl md:text-6xl font-bold font-mono">Tyler Getsay</h1>
            <h2 class="text-xl font-medium">Full Stack Developer interested in startups, economics, & design.</h2>
          </div>
        </div>

        <div class="py-4">
          <div class="flex hidden-print items-center space-x-2">
            <div>
              <font-awesome-icon icon="file"/>
            </div>
            <nuxt-link to="/resume" class="link">
              Resume
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>

    <div class="md:grid gap-5 space-y-2 grid-cols-4">
      <div class="leading-relaxed col-span-4">
        <h4 class="section-header">
          About Me
        </h4>
        <p>
          I am a 10+ year software developer living in the Cincinnati area. I build full stack applications in a fraction of the time as others by leveraging years of experience with my environment and every bit of the modern web/mobile application stack.
        </p>
      </div>
      <div class="col-span-4">
        <h4 class="section-header break">
          What I Can Do For You
        </h4>
        <p>
          If you are an industry expert looking to scale your existing business or develop a new software offering, I have the skills and network necessary to bring your vision to a reality. Utilizing a lean-startup approach, I focus on building exactly what is necessary to prove the concept at minimal development time and cost.
        </p>
      </div>
    </div>

  </div>
</template>

<script>
import moment from "moment";

const faGrapQl = {
  prefix: 'fac',
  iconName: 'graphql', // Any name you like
  icon: [
    400, // width
    400, // height
    [], // ligatures
    '', // unicode (if relevant)
    'M57.468 302.66l-14.376-8.3 160.15-277.38 14.376 8.3z M39.8 272.2h320.3v16.6H39.8z M206.348 374.026l-160.21-92.5 8.3-14.376 160.21 92.5zM345.522 132.947l-160.21-92.5 8.3-14.376 160.21 92.5z M54.482 132.883l-8.3-14.375 160.21-92.5 8.3 14.376z M342.568 302.663l-160.15-277.38 14.376-8.3 160.15 277.38zM52.5 107.5h16.6v185H52.5zM330.9 107.5h16.6v185h-16.6z M203.522 367l-7.25-12.558 139.34-80.45 7.25 12.557z M369.5 297.9c-9.6 16.7-31 22.4-47.7 12.8-16.7-9.6-22.4-31-12.8-47.7 9.6-16.7 31-22.4 47.7-12.8 16.8 9.7 22.5 31 12.8 47.7M90.9 137c-9.6 16.7-31 22.4-47.7 12.8-16.7-9.6-22.4-31-12.8-47.7 9.6-16.7 31-22.4 47.7-12.8 16.7 9.7 22.4 31 12.8 47.7M30.5 297.9c-9.6-16.7-3.9-38 12.8-47.7 16.7-9.6 38-3.9 47.7 12.8 9.6 16.7 3.9 38-12.8 47.7-16.8 9.6-38.1 3.9-47.7-12.8M309.1 137c-9.6-16.7-3.9-38 12.8-47.7 16.7-9.6 38-3.9 47.7 12.8 9.6 16.7 3.9 38-12.8 47.7-16.7 9.6-38.1 3.9-47.7-12.8M200 395.8c-19.3 0-34.9-15.6-34.9-34.9 0-19.3 15.6-34.9 34.9-34.9 19.3 0 34.9 15.6 34.9 34.9 0 19.2-15.6 34.9-34.9 34.9M200 74c-19.3 0-34.9-15.6-34.9-34.9 0-19.3 15.6-34.9 34.9-34.9 19.3 0 34.9 15.6 34.9 34.9 0 19.3-15.6 34.9-34.9 34.9' // svg path data
  ]
}

export default {
  name: "resume",
  methods: {
    download() {
      window.print();
    }
  },
  data() {
    return {
      technologies: [
        {
          name: 'Javascript',
          level: 'Advanced',
          icon: ['fab', 'js']
        },
        {
          name: 'NodeJS',
          level: 'Advanced',
          icon: ['fab', 'node']
        },
        {
          name: 'VueJS',
          level: 'Advanced',
          icon: ['fab', 'vuejs']
        },
        {
          name: 'CSS3',
          level: 'Advanced',
          icon: ['fab', 'css3']
        },
        {
          name: "PHP",
          level: 'Advanced',
          icon: ['fab', 'php']
        },
        {
          name: "Laravel",
          level: 'Advanced',
          icon: ['fab', 'laravel']
        },
        {
          name: "AWS & CDK",
          level: 'Advanced',
          icon: ['fab', 'aws']
        },
        {
          name: "Android",
          level: 'Advanced',
          icon: ['fab', 'android']
        },
        {
          name: "Chrome Extensions",
          level: 'Advanced',
          icon: ['fab', 'chrome']
        },
        {
          name: "Jenkins (CI & CD)",
          level: 'Advanced',
          icon: ['fab', 'jenkins']
        },
        {
          name: "GraphQL",
          level: 'Advanced',
          icon:  faGrapQl
        },
        {
          name: "Flutter",
          level: 'Novice',
          icon: 'mobile'
        },
        {
          name: "React",
          level: 'Novice',
          icon: ['fab', 'react']
        },
        {
          name: "Python",
          level: 'Novice',
          icon: ['fab', 'python']
        },
        {
          name: "Blockchains",
          level: 'Hobbyist',
          icon: ['fab', 'bitcoin']
        },
      ],
      experience: [
        {
          title: "Lead Architect",
          start: moment('09-01-2018'),
          company: "Visitu",
          url: "https://visitu.com",
          description: "I joined Visitu in September of 2018 to help accelerate product development and build a team of developers who are passionate about campus safety. Since arriving I have led the development team through building the next generation of our core products, the launch of these products, and the continued support of them."
        },
        {
          title: "Software Developer",
          start: moment('08-01-2016'),
          finish: moment('09-01-2018'),
          company: "MedaCheck",
          url: "https://medacheck.com",
          description: "Throughout my years at MedaCheck I built many solutions surrounding medication adherence, Bluetooth health monitors, real-time dashboards, and mobility management solutions. Additional knowledge gained involved HIPAA compliance, SOC2 compliance, and UX design. Our solutions were used by area hospitals in IRB approved studies. Primary languages and tools used were NodeJS, Laravel/Symfony (PHP), Android, Python, VueJS, EmberJS, CircleCI, and AWS ElasticBeanstalk."
        },
        {
          title: "Co-Founder & CTO",
          start: moment('12-01-2015'),
          finish: moment('12-01-2016'),
          company: "Fanvester",
          url: "https://www.wcpo.com/news/insider/new-business-fanvestor",
          description: "I built a crowdfunding-based ticketing platform on Laravel, a popular PHP-MVC framework. The application is robust, featuring many third party integrations and backend management features. I also acted the role of tech visionary for the company."
        },
        {
          title: "Freelancer",
          start: moment('01-01-2005'),
          company: "Fanvester",
          url: "https://tylergetsay.com",
          description: "I have helped many small to medium size businesses navigate the growing web landscape; this has manifested in many websites, apps, and internal tools which have been used by millions of users; and subsequently produced millions of dollars in revenue."
        }
      ]
    }
  }
}
</script>

<style scoped>
.section-header {
  @apply text-3xl font-bold mb-4;
}
</style>
