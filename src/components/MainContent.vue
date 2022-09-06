<template>
  <div class="content">
    <div class="container d-flex content-container">

        <div class="stories-post d-flex flex-column">
            <div class="stories">

            </div>
            
            <div class="post">

            </div>
        </div>

        <div class="other">
            
        </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'MainContent',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.content {
    padding: 150px 0;
}

.content-container {
    gap: 30px;
}

.stories-post {
    background-color: blue;
    width: 55%;
    height: 1000px;
    gap: 50px;

    .stories {
        background-color: red;
        width: 100%;
        height: 70px;
        padding: 20px 10px;
    }

    .post {
        background-color: green;
        width: 100%;
        height: 150px;
        padding: 20px 10px;
    }
}

.other {
    background-color: yellow;
    width: 45%;
    height: 1000px;
}

</style>