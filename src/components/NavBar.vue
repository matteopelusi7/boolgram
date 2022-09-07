<template>
  <div class="navbar">
    <nav class="container d-flex align-items-center justify-between">
      <li>
        <figure class="wrap-logo m-auto">
          <img class="logo" src="../assets/logo.png" alt="">
        </figure>
      </li>
      <li>
        <div class="col-auto">
          <label for="search" class="visually-hidden">Cerca</label>
          <input type="text" class="form-control" id="search" placeholder="Cerca">
      </div>
      </li>
      <li>
        <div class="profile">
          <ul class="d-flex align-items-center m-auto list-wrapper">
            <li>
              <img src="https://img.icons8.com/ios-glyphs/344/like--v2.png" width="18px" alt="">
            </li>
            <li>
              <img src="https://img.icons8.com/ios-filled/344/home.png" width="18px" alt="">
            </li>
            <li class="">
              <img class="img-profile" src="../assets/profile.jpg" width="30px" alt="">
            </li>
          </ul>
        </div>
      </li>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

.navbar {
  background-color: white;
  border-bottom: 1px solid lightgray;
  width: 100%;
  height: 60px;
  position: fixed;
}

.form-control {
  text-align: center;
  padding: 4px 30px;
  border-radius: 0px;
  border: 1px solid lightgray;
  font-size: 14px;
}

.logo {
  width: 80px;
}

.list-wrapper {
  gap: 22px;
}

.img-profile {
  border-radius: 999px;
}

.profile img, .logo {
  cursor: pointer;
}

li {
  list-style: none;
}

</style>