<template>
  <div>
    <div class="mb-6">
      <h1 class="font-medium">Awesome lists</h1>
    </div>
    <ol class="space-y-2 list-disc list-inside">
      <li>
        <nuxt-link to="/awesome/books" class="text-blue-500 underline">
          Books
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/awesome/podcasts" class="text-blue-500 underline">
          Podcasts
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/awesome/posts" class="text-blue-500 underline">
          Posts / Articles
        </nuxt-link>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: "index"
}
</script>

<style scoped>

</style>
