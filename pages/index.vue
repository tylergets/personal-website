<template>
  <div class="mx-auto max-w-7xl p-5">
    <div class="flex items-center pb-5">
      <div class="pr-10 pl-8">
        <img class="h-32" src="~/assets/portrait.svg"/>
      </div>
      <div>
        <div class="md:flex justify-between items-center">
          <div class="space-y-4">
            <h1 class="text-5xl md:text-6xl font-bold font-mono">Tyler Getsay</h1>
            <h2 class="text-xl font-medium">Full Stack Developer interested in startups, economics, & design.</h2>
          </div>
        </div>

        <div class="py-4 space-x-4 flex">
          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon class="text-blue-500" :icon="['fab', 'twitter']"/>
            </div>
            <a target="_blank" href="https://twitter.com/tylergets" class="link">
              Twitter
            </a>
          </div>

          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon class="text-blue-500" :icon="['fab', 'github']"/>
            </div>
            <a target="_blank" href="https://github.com/tylergets" class="link">
              GitHub
            </a>
          </div>

          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon class="text-blue-500" :icon="['fab', 'linkedin']"/>
            </div>
            <a target="_blank" href="https://www.linkedin.com/in/tylergetsay/" class="link">
              LinkedIn
            </a>
          </div>

          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon class="text-blue-500" icon="file"/>
            </div>
            <nuxt-link to="/resume" class="link">
              Resume
            </nuxt-link>
          </div>

          <div class="flex items-center space-x-2">
            <div>
              <font-awesome-icon class="text-blue-500" icon="gifts"/>
            </div>
            <nuxt-link to="/awesome" class="link">
              Awesome
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
    </div>

  </div>
</template>

<script>

export default {
  layout: 'full'
}
</script>

<style scoped>
.section-header {
  @apply text-3xl font-bold mb-4;
}
</style>
