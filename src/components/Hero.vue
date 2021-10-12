<template>
  <div id="hero">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-4 col-left">
          <h1>Complete Your Dreams in JavaS Programming</h1>
          <p>Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.</p>
          <a href="#" class="btn">
            <h6>Download free E-book</h6>
          </a>
        </div>
        <div class="col-8 col-right">
          <img src="../assets/materiale/images/home-5-hero-image.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Hero',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#hero {
  position: relative;
  overflow: hidden;
  padding: 20px 0px;
  background-color: var(--oneColor);
  border: 1px solid black;
}

#hero::before {
  content: "";
  position: absolute;
  bottom: 0px;
  left: 0px;
  width: 100%;
  height: 80%;
  z-index: -10px;
  background-image: url("../assets/materiale/jumbo-overlay.svg");
  background-repeat: repeat;
  background-position: center;
  background-size: cover;
  transform: rotate(180deg);
}

.col-left {
  border: 1px solid black;
}
.col-right {
  text-align: right;
  border: 1px solid black;
}
.col-right img {
  position: relative;
  z-index: 10px;
  width: 70%;
  border: 1px solid black;
}
</style>
