<template>
    <div class="stories-post d-flex flex-column">
        <div class="stories">
            <ul class="wrap-stories d-flex align-items-center justify-content-center m-0 p-0 flex-wrap">
                <li v-for="(storie, i) in stories" :key="i" class="cursor-pointer list">
                    <img class="logo-profile" :src="storie.profile_picture" width="60px" height="60px" alt="">
                    <p>{{ storie.profile_name }}</p>
                </li>
            </ul>
        </div>

        <div v-for="(post, i) in posts" :key="i" class="post">
            <div class="name-profile d-flex align-items-center justify-content-between py-3 px-3">
                <div class="gap-3 wrap-profile d-flex align-items-center pl-0">
                    <img class="logo-profile" :src="post.profile_picture" width="45px" height="45px" alt="">
                    <p class="m-0 p-0">{{ post.profile_fullname }}</p>
                </div>
                <div class="dot">
                    <img src="https://img.icons8.com/ios-glyphs/344/more.png" width="20px" alt="">
                </div>
            </div>
            <div class="image-content">
                <img class="content-image" :src="post.post_image" width="100%" alt="">
            </div>
            <div class="other-post">
                <div class="icon p-3 d-flex align-items-center justify-content-start gap-2">
                    <img src="https://img.icons8.com/ios-glyphs/344/like--v2.png" width="25px" alt="">
                    <img src="https://img.icons8.com/ios/344/topic.png" width="25px" alt="">
                </div>
                <div class="likes d-flex align-items-center gap-2 px-3 py-2">
                    <img class="img-profile" :src="post.likes[0].profile_picture" width="20px" height="20px" alt="">
                    <p class="p-0 m-0 text-start">Piace a <span class="fw-bold">{{ post.likes[0].username }}</span> e <span class="fw-bold">{{ post.likes.length }} altri</span></p>
                </div>
                <div class="comments d-flex align-items-center px-3 py-2">
                    <p class="p-0 m-0 text-start"><span class="fw-bold">{{ post.comments[0].username }}</span><span> {{ post.comments[0].text }}</span></p>
                </div>
                <div class="other-comments d-flex align-items-center px-3 py-2">
                    <p class="p-0 m-0 text-start text-fx">Mostra tutti e <span>{{ post.comments.length }}</span> i commenti</p>
                </div>
                <div v-for="(comment,i) in post.comments" :key="i" class="comments align-items-center p-0 m-0 px-3 py-2">
                    <p v-if="comment.username.length" class="p-0 m-0 text-start"><span class="fw-bold">{{ comment.username }}</span><span> {{ comment.text }}</span></p>
                </div>
                <div class="times p-3">
                    <p class="m-0 p-0 text-start text-fx">33 ore fa</p>
                </div>
                <div class="write fs-6 d-flex align-items-center justify-content-between px-3 py-3">
                    <div>
                        <p class="p-0 m-0 text-start text-fx">Aggiungi un commento</p>
                    </div>
                    <div>
                        <p class="p-0 m-0 text-start text-primary">Pubblica</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

import axios from 'axios';

export default {
  name: 'MainPost',
  data() {
    return {
        stories: [],
        posts: []
    }
  },
  methods: {
    fetchStories: function() {
        axios.get('https://flynn.boolean.careers/exercises/api/boolgram/profiles')
        .then( res => {
            this.stories = res.data
            console.log(this.stories)
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

li {
    list-style: none;
}

.text-fx {
    color: rgb(156, 156, 156);
}

.logo-profile {
    border-radius: 999px;
    border: 2px solid purple;
    padding: 2px;
}


.img-profile {
    border-radius: 999px;
}

.write {
    border-top: 1px solid lightgray;
}

.wrap-stories {
    gap: 50px;
}

.stories-post {
    width: 55%;
    gap: 50px;

    .stories {
        width: 100%;
        padding: 35px;
        border: 2px solid lightgray;
    }

    .post {
        border: 2px solid lightgray;
        width: 100%;
    }
}

.stories p {
    margin-top: 10px;
    font-size: 12px;
}

.list {
    cursor: pointer;
}

</style>