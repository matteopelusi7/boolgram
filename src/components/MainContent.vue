<template>
  <div class="content">
    <div class="container d-flex content-container">

        <MainPost />

        <MainOther />

    </div>
  </div>
</template>

<script>

import MainPost from '../components/MainPost.vue';
import MainOther from '../components/MainOther.vue';

export default {
  name: 'MainContent',
  components: {
    MainPost,
    MainOther
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