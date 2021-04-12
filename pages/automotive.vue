<template>
<div>
  <div class="container">
    <div>
      <div class="titleContainer">
        <h1 class="title">
          qwertypants.net
        </h1>
      </div>
      <Header />
    </div>
  </div>
    <div class="stories">
      <section class="story">
        <Story
            v-for="story in stories"
            :key="story.id"
            :id="story.id"
            :title="story.title"
            :previewText="story.previewText"
            :b="story.b"
        />
      </section>
    </div>
  </div>
</template>

<script>
import Story from '@/components/Story'
export default {
    components: {
        Story
    },
    asyncData() {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            stories: [
              {
                id: "0",
                title: "Milky and the Power FC",
                previewText: "Remember when your car wasn't broken?",
                b: "smokeshow"
              },
              {
                id: "1",
                title: "There were once 3",
                previewText: "The tale of the Asphalt Assassins",
                b: "skittles"
              },
              {
                id: "2",
                title: "Calder log",
                previewText: "Pondering the mysteries of the race boot...",
                b: "calder_sit"
              },
              {
                id: "3",
                title: "Faulty push rod on Steven's streeter",
                previewText: "Fixing the mistake of a reputable tuning shop",
                b: "VE_lifters"
              },
              {
                id: "4",
                title: "Gearbox blows up at Winton",
                previewText: "You'd think the rain would keep the gearbox demons at bay...",
                b: "milky_winton"
              },
              {
                id: "5",
                title: "Installing Dash into Mila's S15",
                previewText: "The street car got some love",
                b: "s15"
              },
              {
                id: "6",
                title: "V8 Oil Pressure Issues",
                previewText: "Steven was having some issues with oil pressure at Winton. We logged to see just how much",
                b: "phteven"
              },
            ]
          })
        }, 1500)
      })
    }
}
</script>



<style scoped>
.story {
    display: flex;
    flex-flow: row wrap;
    justify-content: left;
    align-items: left;
}

.thumbnail {
    background-position: center;
    background-size: cover;
}

.stories {
    margin-left: 150px;
    margin-right: 150px;
    margin-top: 50px;
    margin-bottom: 50px;
}
</style>