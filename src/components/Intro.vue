<template>
  <section id="intro" class="container">
    <div class="row">
      <div class="col-12 title-1">
        <p>START LEARNING CODING LANGUAGES</p>
        <h3>Build Your Dram </h3><span> TODAY</span>
      </div>
    </div>
    <div class="row dream">
      <div v-for="(dream, index) in dreams" :key="index" class="col-12 col-md-3">
        <div class="dream-img">
          <img :src="require(`../assets/materiale/images/${dream.image}`)" alt="">
        </div>
        <h4>{{dream.title}}</h4>
        <p>{{dream.description}}</p>
        <a href="#" class="btn btn-2">Start now 
          <i class="fas fa-long-arrow-alt-right"></i>
        </a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Intro',
  data()  {
    return {
      dreams: [
        {
          "image": "home-5-image-box-01.png",
          "title": "Ideal Discussion",
          "description": "Get tearned up with the specialists who work and teach coding for years at famous universities.",
        },
        {
          "image": "home-5-image-box-02.png",
          "title": "Web Development",
          "description": "Learn to start building a webpage from scratch. You decide your own pace, course and speed.",
        },
        {
          "image": "home-5-image-box-03.png",
          "title": "System Administration",
          "description": "Learnes are encouraged to study the mechanism and structure of system admistration.",
        },
        {
          "image": "home-5-image-box-04.png",
          "title": "Graphic Design",
          "description": "Have a passion for graphic and arts? Show your talents with confidence and self-assertiveness.",
        },
      ]
    }
  }
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.title-1 {
  text-align: center;
  margin: 2.5rem 0rem;
  p {
    font-size: .75rem;
    letter-spacing: .0625rem;
  }
  h3 {
    display: inline-block;
    font-size: 1.5rem;
    color: var(--twoColor);
  }
  span {
    color: var(--threeColor);
    font-size: 1.5rem;
    font-weight: normal;
  }
}

.dream .col-12 {
  text-align: center;
  margin: 1.25rem 0rem;
  .dream-img {
    width: 100%;
    height: 12.5rem;
  }
  img {
    object-fit: contain;
    object-position: center;
    width: 70%;
    height: 100%;
  }
}

.dream h4 {
  margin: .625rem 0rem;
}
.dream p {
  line-height: 1.5rem;
}

.btn i {
  vertical-align: middle;
  margin-left: .5rem;
}
</style>
