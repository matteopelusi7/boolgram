<template>
    <div class="other">
        <div>
            <ul class="pfirst d-flex align-items-center justify-content-between m-0 p-5">
                <li>
                    <img class="img-profile" src="../assets/profile.jpg" width="55px" alt="">
                </li>
                <li class="d-flex flex-column align-items-center justify-content-center">
                    <p class="p-0 m-0">matteopelusi7</p>
                    <p class="p-0 m-0 text-fx">Matteo Pelusi</p>
                </li>
                <li>
                    <p class="p-0 m-0 text-primary">Passa a</p>
                </li>
            </ul>
        </div>
        <div>
            <div class="psecond d-flex align-items-center justify-content-between p-5">
                <p class="m-0 p-0 text-fx">Suggerimenti per te</p>
                <p class="m-0 p-0 fw-bold">Mostra tutti</p>
            </div>
            <div>
                <ul class="px-5">
                    <li v-for="(storie, i) in stories" :key="i" class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" :src="storie.profile_picture" width="60px" height="60px" alt="">
                            <p class="m-0 p-0 fw-bold">{{ storie.profile_name }}</p>
                        </div>
                        <div>
                            <p class="ptird m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                </ul>
            </div>
        </div>
        <div class="px-5 mt-5 text-start">
            <p class="m-0 p-0 text-fx text-uppercase">&copy; Boolgram from Facebook</p>
        </div>
    </div>
</template>

<script>

import axios from 'axios';

export default {
  name: 'MainOther',
  data() {
    return {
        stories: [],
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
  },
  created() {
    this.fetchStories();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.other {
    width: 45%;
}

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

.name-profile {
    gap: 20px;
}

.content-image {
    object-fit: cover;
    object-position: center;
}

.name-profile p {
    font-weight: 700;
}

@media all and (max-width: 995px) {

    .pfirst {
        display: flex;
        flex-direction: column;
        gap: 30px;
    }

    .psecond {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .ptird {
        display: none;
    }

}

</style>