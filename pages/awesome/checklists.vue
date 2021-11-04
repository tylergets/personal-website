<template>
  <div class="space-y-4">
    <div>
      A list of good checklists
    </div>
    <ul class="mt-4 space-y-2 list-disc list-inside">
      <li v-for="item in list" >
        <a :href="item.url" target="_blank" class="text-blue-500 underline">
          {{item.title}}
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
      list: [
        {
          title:"Minimum Viable Secure Product",
          url:"https://www.sideprojectchecklist.com/marketing-checklist/"
        },
        {
          title: "Side Project Marketing Checklist",
          url: "https://www.sideprojectchecklist.com/marketing-checklist/",
        },
        {
          title: "Side Project Sales Checklist",
          url: "https://www.sideprojectchecklist.com/sales-checklist/"
        }
      ]
    };
  }
}
</script>

<style scoped>

</style>
