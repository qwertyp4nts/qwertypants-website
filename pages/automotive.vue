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
    <div class="storyContainer">
        <section class="stories">
            <Story title="V8 Oil Pressure Issues" 
            previewText="Steven was having some issues with oil pressure at Winton. We logged to see just how much"
            b='phteven'/>
            <Story title="Installing Dash into Mila's S15" 
            previewText="The street car got some love"
            b='s15'/>
            <Story title="Gearbox blows up at Winton" 
            previewText="You'd think the rain would keep the gearbox demons at bay..."
            b='milky_winton'/>
            <Story title="Faulty push rod on Steven's streeter" 
            previewText="Fixing the mistake of a reputable tuning shop"
            b='VE_lifters'/>
            <Story title="Calder log" 
            previewText="Pondering the mysteries of the race boot..."
            b='calder_sit'/>
            <Story title="There were once 3" 
            previewText="The tale of the Asphalt Assassins"
            b='skittles'/>
            <Story title="Milky and the Power FC" 
            previewText="Remember when your car wasn't broken?"
            b='smokeshow'/>
        </section>
    </div>
  </div>
</template>

<script>
import Story from '@/components/Story'
export default {
    components: {
        Story
    }
}
</script>



<style scoped>
.stories {
    display: flex;
    flex-flow: row wrap;
    justify-content: left;
    align-items: left;
}

.thumbnail {
    background-position: center;
    background-size: cover;
}

.storyContainer {
    margin-left: 150px;
    margin-right: 150px;
    margin-top: 50px;
    margin-bottom: 50px;
}
</style>