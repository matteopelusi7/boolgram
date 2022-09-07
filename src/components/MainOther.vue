<template>
    <div class="other">
        <div>
            <ul class="d-flex align-items-center justify-content-between m-0 p-5">
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
            <div class="d-flex align-items-center justify-content-between p-5">
                <p class="m-0 p-0 text-fx">Suggerimenti per te</p>
                <p class="m-0 p-0 fw-bold">Mostra tutti</p>
            </div>
            <div>
                <ul class="px-5">
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
                        </div>
                    </li>
                    <li class="d-flex align-items-center justify-content-between mb-3 p-0">
                        <div class="gap-3 d-flex align-items-center justify-content-between">
                            <img class="logo-profile" src="../assets/landscape.png" width="60px" alt="">
                            <p class="m-0 p-0 fw-bold">estamte</p>
                        </div>
                        <div>
                            <p class="m-0 p-0 text-primary">Segui</p>
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
export default {
  name: 'MainOther',
  
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

</style>