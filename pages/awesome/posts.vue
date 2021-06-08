<template>
  <div class="space-y-4">
    <div>
      Here is a list of posts I like
    </div>
    <ul class="mt-4 space-y-2 list-disc list-inside">
      <li v-for="item in list" >
        <a :href="item.link" target="_blank" class="text-blue-500 underline">
          {{item.name}}
        </a>
      </li>
    </ul>

  </div>
</template>

<script>
export default {
  head: {
    title: 'Books'
  },
  data() {
    return {
      wanted: [],
      list: [
        {
          name: 'MIBS Simplified Rules of Coordinated Consensus through Chaos',
          link: 'https://wiki.hacdc.org/index.php?title=MIBS_Simplified_Rules_of_Coordinated_Consensus_through_Chaos'
        }
      ]
    };
  }
}
</script>

<style scoped>

</style>
