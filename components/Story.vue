<template>
    <nuxt-link :to="'/story/' + id">
        <article class="story">
            <div class="thumbnail" :style="{backgroundImage: 'url(' + cyberImg + ')'}"></div>
            <h1>{{ title }}</h1>
            <p>{{ previewText }}</p>
        </article>
    </nuxt-link>
</template>

<script>
export default {
    props: ['title', 'previewText', 'b', 'id'],

computed: {
  cyberImg() {
    return require('../assets/' + this.b + '.jpg') 
  }
}

}
</script>

<style scoped>

a {
    text-decoration: none;
    color: #D1BCE3;
}

.thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 300px;
    margin-bottom: 10px;
}

.story {
    box-sizing: border-box;
    width: 450px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #aaa;
    margin: 10px;
}
</style>