<template>
  <div class="p-5">

    <div class="mx-auto max-w-7xl ">
      <div class="flex pb-1">
        <div class="pr-10 pl-8 hidden md:block">
          <img class="h-16" src="~/assets/portrait.svg"/>
        </div>
        <div>
          <div class="">
            <div class="">
              <h1 class="text-xl font-bold font-mono">Tyler Getsay - <span class="text-xl font-medium">Full Stack Developer interested in startups, economics, & design.</span></h1>
            </div>
          </div>

          <div class="space-x-4 pt-2 flex">
            <div class="flex items-center space-x-2">
              <div>
                <font-awesome-icon class="text-blue-500" :icon="'home'"/>
              </div>
              <nuxt-link to="/" class="link">
                Home
              </nuxt-link>
            </div>

            <div class="flex items-center space-x-2">
              <div>
                <font-awesome-icon class="text-blue-500" :icon="['fab', 'twitter']"/>
              </div>
              <a target="_blank" href="https://twitter.com/tylergets" class="link">
                Twitter
              </a>
            </div>
          </div>


          <div class="pt-4">
            <NuxtContent
              class="prose prose-sm max-w-none"
              :document="document"
            />
          </div>
        </div>
      </div>
    </div>



    <div class="max-w-7xl mx-auto">

    </div>


  </div>

</template>

<script>
export default {
  layout: 'full',
  async asyncData({ $content, route }) {

    const document = await $content(route.params.page).fetch();

    return { document };
  }
}
</script>

<style scoped>

</style>
