<template>
    <div class="stories-post d-flex flex-column">
        <div class="stories">
            <ul class="wrap-stories d-flex align-items-center justify-content-between m-0 p-0">
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>estamte</p>
                </li>
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>trunte</p>
                </li>
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>wolf</p>
                </li>
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>calind</p>
                </li>
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>calind</p>
                </li>
                <li>
                    <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                    <p>calind</p>
                </li>
            </ul>
        </div>

        <div class="post">
            <div class="name-profile d-flex align-items-center justify-content-between py-3 px-3">
                <div class="gap-3 wrap-profile d-flex align-items-center pl-0">
                    <img class="logo-profile" src="../assets/landscape.png" width="45px" alt="">
                    <p class="m-0 p-0">Wolf</p>
                </div>
                <div class="dot">
                    <img src="https://img.icons8.com/ios-glyphs/344/more.png" width="20px" alt="">
                </div>
            </div>
            <div class="image-content">
                <img class="content-image" src="../assets/landscape.png" width="100%" alt="">
            </div>
            <div class="other-post">
                <div class="icon p-3 d-flex align-items-center justify-content-start gap-2">
                    <img src="https://img.icons8.com/ios-glyphs/344/like--v2.png" width="25px" alt="">
                    <img src="https://img.icons8.com/ios/344/topic.png" width="25px" alt="">
                </div>
                <div class="likes d-flex align-items-center gap-2 px-3 py-2">
                    <img class="img-profile" src="../assets/profile.jpg" width="20px" alt="">
                    <p class="p-0 m-0 text-start">Piace a <span class="fw-bold">cadin</span> e <span class="fw-bold">4 altri</span></p>
                </div>
                <div class="comments d-flex align-items-center px-3 py-2">
                    <p class="p-0 m-0 text-start"><span class="fw-bold">wolf</span><span> queen of all</span></p>
                </div>
                <div class="other-comments d-flex align-items-center px-3 py-2">
                    <p class="p-0 m-0 text-start text-fx">Mostra tutti e <span>4</span> i commenti</p>
                </div>
                <div class="comments align-items-center p-0 m-0 px-3 py-2">
                    <p class="p-0 m-0 text-start"><span class="fw-bold">cadin</span><span> whatt!!</span></p>
                    <p class="p-0 m-0 text-start"><span class="fw-bold">trunt</span><span> wow</span></p>
                    <p class="p-0 m-0 text-start"><span class="fw-bold">berds</span><span> queen</span></p>
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
export default {
  name: 'MainPost',
  
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

</style>