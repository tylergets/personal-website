<template>
  <div class="mx-auto max-w-7xl p-5">
    <div class="md:flex justify-between items-center mb-3">
      <div class="space-y-4">
        <h1 class="text-5xl md:text-6xl font-bold font-mono">Tyler Getsay</h1>
        <h2 class="text-xl font-medium">Full Stack Developer interested in startups, economics, & design.</h2>
        <h3 class="flex items-center space-x-4 pb-2">
          <div>
            <font-awesome-icon class="text-green-500 text-2xl" icon="map-marker"/>
          </div>
          <div class="">
            <div class="font-medium">Cincinnati, Ohio</div>
            <div class="text-gray-500">Looking to explore new places!</div>
          </div>
        </h3>
      </div>
      <div>
        <div class="flex flex-col space-y-2">
          <a href="https://tylergetsay.com" class="link hidden-screen" target="_blank">
            https://tylergetsay.com
          </a>
          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon icon="at"/>
            </div>
            <a href="mailto:tylergetsay@gmail.com" class="link">
              tylergetsay@gmail.com
            </a>
          </div>
          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon :icon="['fab','twitter']"/>
            </div>
            <a href="https://twitter.com/tylergets" class="link">
              @TylerGets
            </a>
          </div><div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon :icon="['fab','github']"/>
            </div>
            <a href="http://github.com/tylergets" class="link">
              @TylerGets
            </a>
          </div><div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon icon="phone"/>
            </div>
            <a href="tel:+14404094081" class="link">
              +1 (440) 409-4081
            </a>
          </div>
          <div class="flex hidden-print items-center space-x-2">
            <div>
              <font-awesome-icon :icon="'file-pdf'"/>
            </div>
            <a class="link " @click="download">
              Download as PDF
            </a>
          </div>


        </div>
      </div>
    </div>
    <div class="md:grid gap-5 space-y-4 grid-cols-4">
      <div class="leading-relaxed col-span-4">
        <h4 class="section-header">
          About Me
        </h4>
        <p>
          I am a 10+ year software developer living in the Cincinnati area. I build full stack applications in a fraction of the time as others by leveraging years of experience with my environment and every bit of the modern web/mobile application stack.
        </p>
      </div>
      <div class="col-span-3">
        <h4 class="section-header">
          Experience
        </h4>
        <div class="space-y-4">
          <div v-for="job in experience" class="flex flex-col space-y-1">
            <h5><span class="font-bold">{{job.title}}</span> - <a class="link" :href="job.url" rel="noreferrer">{{job.company}}</a></h5>
            <div class="text-gray-700">
              <span v-if="job.start">{{$moment(job.start).format('MMM YYYY')}}</span>
              <span v-if="job.finish"> - {{$moment(job.finish).format('MMM YYYY')}}</span>
              <span v-else> - Present</span>
            </div>
            <p class="">
              {{ job.description }}
            </p>
          </div>
        </div>
      </div>
      <div class="col-span-3">
        <h4 class="section-header break">
          Before Code
        </h4>
        <p>
          Before entering the world of software development and entrepreneurship, I worked as a commissioned sales representative for various industries. Its through these experience that I pull out some of my core principals which I continue to use not only at work but day-to-day life; the skills I developed around building relationships, delivering value, and education are what sets me apart today.
        </p>
      </div>
      <div class="col-span-3">
        <h4 class="section-header break">
          Ways I Can Help
        </h4>
        <p>
          Whether you are having issues scaling an existing product, or want to bring something new to the market; I have the experience to take it from whiteboard to app store, without endless meetings that cost you time and money.
        </p>
      </div>
<!--      <div class="col-span-3">-->
<!--        <h4 class="section-header break">-->
<!--          Projects-->
<!--        </h4>-->
<!--        <div class="space-y-1">-->
<!--          <div class="flex flex-col space-y-1">-->
<!--            <h5><span class="font-bold">University of Cincinnati</span></h5>-->
<!--            <div class="text-gray-700">-->
<!--              <span>{{$moment('08/01/2014').format('MMM YYYY')}}</span>-->
<!--              <span> - {{$moment('08/01/2019').format('MMM YYYY')}}</span>-->
<!--            </div>-->
<!--            <p>-->
<!--              I decided to go to-->
<!--            </p>-->
<!--          </div>-->

<!--        </div>-->
<!--      </div>-->
      <div class="md:row-start-2 col-start-4 col-end-4">
        <h4 class="section-header">
          Technologies I Use
        </h4>
        <ul>
          <li class="flex cursor-pointer transform transition ease-in-out hover:scale-110 truncate items-center space-x-2 text-md" v-for="tech in technologies">
            <div class="w-10">
              <font-awesome-icon :icon="tech.icon"/>
            </div>
            <div class="">
              <span>{{tech.name}}</span>
              <span class="text-gray-600 font-light">- {{ tech.level }}</span>
            </div>
          </li>
        </ul>
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
  head: {
    title: 'Resume',
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
