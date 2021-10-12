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
    <div class="row perspective">
      <div class="col-12 col-md-6 col-left">
        <img class="img-esultanza" src="../assets/materiale/images/about-us-03-image-01.png" alt="">
      </div>
      <div class="col-12 col-md-6 col-right">
        <p>DREAM WITH <span>MAXCOACH</span></p>
        <h3>Construct A <span>Stunning</span> Career Perspective</h3>
        <div class="card">
          <div class="header-card active">
            <h4>Multiple Platforms Supported for Teaching & Studying</h4>
            <i class="fas fa-minus-circle"></i>
            <!-- <i class="fas fa-plus-circle"></i> -->
          </div>
          <div class="body-card">
            MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access our knowledge base from any device.
          </div>
        </div>
        <div class="card">
          <div class="header-card">
            <h4>Multiple Course Participation at the Same Time</h4>
            <i class="fas fa-plus-circle"></i>
          </div>
        </div>
        <div class="card">
          <div class="header-card">
            <h4>Track Study Progress & Deliver Prompt Feedback</h4>
            <i class="fas fa-plus-circle"></i>
          </div>
        </div>
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
@import '../assets/style/common';

.title-1 {
  text-align: center;
  margin: 2.5rem 0rem;
  p {
    font-size: .75rem;
    letter-spacing: .0625rem;
  }
 
  h3 {
    @include title-intro;
  }
  span {
    @include span-intro;
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
  padding: .3125rem;
  line-height: 1.5rem;
}

.btn i {
  vertical-align: middle;
  margin-left: .5rem;
}

.perspective {
  .col-left, .col-right {
    margin: .9375rem 0rem;
    padding: 1.25rem;
  }
  .col-left {
    background-image: url("../assets/materiale/underlay-shape-lilla.svg");
    background-repeat: no-repeat;
    background-size: 70%;
    background-position: left;
  }
  .col-right {
    line-height: 2.5rem;
    p {
      color: var(--twoColor);
      font-size: .75rem;
      span {
        font-weight: bold
      }
    }
    h3 {
    @include title-intro;
    span {
      @include span-intro;
    }
    }
  }
}

.img-esultanza {
  width: 80%;
  margin-left: auto;
  display: block;
}

.card {
    margin: 1.5625rem 0rem;
    box-shadow: 0rem .125rem .5rem gray;
    line-height: 1.50rem;
    border-radius: .46875rem;
    overflow: hidden;
  .header-card, .body-card {
    padding: .625rem 1.25rem;
  }
  .header-card {
    display: flex;
    align-items: center;
    justify-content: space-between;
    font-weight: bold;
    opacity: 0.8;
    &.active {
      background-color: var(--threeColor);
      color: white;
      text-shadow: 0rem .125rem .25rem black;
    }
    i {
      margin-left: .3125rem;
      font-size: 1.5rem;
    }
  }
}


</style>
