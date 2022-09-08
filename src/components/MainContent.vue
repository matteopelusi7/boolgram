<template>
  <div class="content">

    <div v-if="loading == true">

      <SkeletonLoading />
      
    </div>

    <div v-else class="container d-flex content-container">

      <MainPost />

      <MainOther />

    </div>
  </div>
</template>

<script>

import axios from 'axios';
import MainPost from '../components/MainPost.vue';
import MainOther from '../components/MainOther.vue';
import SkeletonLoading from '../components/SkeletonLoading.vue';

export default {
  name: 'MainContent',
  components: {
    MainPost,
    MainOther,
    SkeletonLoading
  },
  data() {
    return {
        stories: [],
        posts: [],
        loading: false,
    }
  },
  methods: {
    fetchStories: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/boolgram/profiles')
        .then( res => {
            this.stories = res.data
            console.log(this.stories)
            this.loading == true
        })
        .catch((err) => {
            console.warn(err);
        });
    },
    fetchPost: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/boolgram/posts')
        .then( res => {
            this.posts = res.data
            console.log(this.posts)
            this.loading == true
        })
        .catch((err) => {
            console.warn(err);
        });
    }
  },
  created() {
    this.fetchStories();
    this.fetchPost()
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.content {
    padding: 120px 0;
}

.content-container {
    gap: 30px;
}

</style>