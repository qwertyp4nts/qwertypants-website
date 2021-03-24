<template>
  <div class="container">
    <div>
      <div class="titleContainer">
        <h1 class="title typewriter">
          qwertypants.net
        </h1>
      </div>
      <Header />
      <NasaPic />
    </div>
  </div>
</template>

<script>
import NasaPic from '@/components/NasaPic'
export default {
  components: {
    NasaPic
  },
  head() {
    return {
      title: "Mila's Place",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Mila's brain on a page"
        }
      ]
    };
  }
};
</script>

<style>
.container {
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.titleContainer {
  padding-top: 2rem;
  padding-bottom: 2rem;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  width: 900px;
  letter-spacing: .15em;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.typewriter {
  overflow: hidden; /* Ensures the content is not revealed until the animation */
  border-right: .10em solid orange; /* The typwriter cursor */
  white-space: nowrap; /* Keeps the content on a single line */
  margin: 0 auto; /* Gives that scrolling effect as the typing happens */
  letter-spacing: .15em; /* Adjust as needed */
  animation: 
    typing 3.5s steps(40, end),
    blink-caret .75s step-end infinite;
}

/* The typing effect */
@keyframes typing {
  from { width: 0 }
  to { width: 66% }
}

/* The typewriter cursor effect */
@keyframes blink-caret {
  from, to { border-color: transparent }
  50% { border-color: orange; }
}

</style>
