<template>
  <div class="p-4">
    <div>
      Here is a list of podcasts I like
    </div>
    <ul class="list-disc list-inside">
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
  name: "podcasts",
  data() {
    return {
      list: [
        {
          name: "ALAB Series",
          link: "https://www.alabseries.com/"
        },
        {
          name: "5-4 Podcast",
          link: "https://www.fivefourpod.com/"
        },
        {
          name: "The Adam Carolla Show",
          link: "https://adamcarolla.com/"
        },
        {
          name: "Lex Fridman Show",
          link: "https://lexfridman.com/"
        },
        {
          name: "Darknet Diaries",
          link: "https://darknetdiaries.com/"
        },
        {
          name: "99% Invisible",
          link: "https://99percentinvisible.org/"
        },
        {
          name: "The All In Podcast",
          link: "https://www.allinpodcast.co/"
        },
        {
          name: "Spearhead",
          link: "https://spearhead.co/"
        },
        {
          name: "Below the Line",
          link: "https://belowthelinepod.com/"
        },
        {
          name: "Making Sense with Sam Harris",
          link: "https://samharris.org/podcast/"
        },
        {
          name: "This Week In Startups",
          link: "https://thisweekinstartups.com/"
        },
        {
          name: "Paradox Podcast",
          link: "https://paradoxpodcast.co/"
        },
        {
          name: "Ear Hustle",
          link: "https://www.earhustlesq.com/"
        },
        {
          name: "Naval",
          link: "https://nav.al/"
        },
    }
  }
}
</script>

<style scoped>

</style>
