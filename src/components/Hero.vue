<template>
  <div id="hero">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-12 col-md-4 col-left">
          <h1>Complete Your Dreams in JavaS Programming</h1>
          <p class="description">Learn any coding program in distance and for a reasonable fee. You don't have to struggle alone, you've got our assistance and help.</p>
          <a href="#" class="btn btn-1">
              <i class="fas fa-download"></i>
              Download free E-book              
          </a>
        </div>
        <div class="col-12 col-md-8 col-right">
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
  padding: 1.25rem 0rem;
  background-color: var(--oneColor);
}

#hero::before {
  content: "";
  position: absolute;
  bottom: 0rem;
  left: 0rem;
  width: 100%;
  height: 60%;
  z-index: -0.625rem;
  background-image: url("../assets/materiale/jumbo-overlay.svg");
  background-repeat: repeat;
  background-position: center;
  background-size: cover;
  transform: rotate(180deg);
}

h1 {
  line-height: 2.375rem;
  color: var(--twoColor);
  margin-bottom: 1.25rem;
}

.description {
  margin-bottom: 1.25rem;
}

.btn i {
  margin-right: .5rem;
  vertical-align: middle;
}

.col-right {
  display: flex;
  justify-content: right;
}
.col-right img {
  position: relative;
  z-index: .625rem;
  width: 65%;
}
</style>
