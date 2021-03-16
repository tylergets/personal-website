<template>
  <div class="space-y-4">
    <div>
      Here is a list of books I like
    </div>
    <ul class="mt-4 space-y-2 list-disc list-inside">
      <li v-for="item in list" >
        <a :href="item.link" target="_blank" class="text-blue-500 underline">
          {{item.name}}
        </a>
        - <span class="italic">{{item.author}}</span>
      </li>
    </ul>

    <div v-if="wanted.length > 0">
      Books I plan on reading
    </div>
    <ul class="mt-4 list-disc list-inside">
      <li v-for="item in wanted" >
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
          name: 'Economics For The Common Good',
          author: 'Jean Tirole',
          link: 'https://press.princeton.edu/books/hardcover/9780691175164/economics-for-the-common-good'
        },
        {
          name: 'The Hard Thing About Hard Things',
          author: 'Ben Horowitz',
          link: 'https://www.amazon.com/Hard-Thing-About-Things-Building/dp/0062273205'
        },
        {
          name: 'Zero to One',
          author: 'Peter Thiel',
          link: 'https://en.wikipedia.org/wiki/Zero_to_One'
        },
        {
          name: 'Moral Mazes',
          author: 'Robert Jackall',
          link: 'https://en.wikipedia.org/wiki/Moral_Mazes'
        },
        {
          name: 'Deep Work',
          author: 'Cal Newport',
          link: 'https://www.amazon.com/Deep-Work-Focused-Success-Distracted/dp/1455586692'
        },
        {
          name: 'In The Realm Of Hungry Ghosts',
          author: 'Gabor Mate',
          link: 'https://www.amazon.com/Realm-Hungry-Ghosts-Encounters-Addiction'
        }
      ]
    };
  }
}
</script>

<style scoped>

</style>
