<template>
  <section id="about-us">
    <div class="container">
      <div class="row">
        <div class="col-12 title">
          <p>PEOPLE ARE PRAISING MAXCOACH</p>
          <h3>What make they <span>love us?</span></h3>
        </div>
      </div>
      <div class="row container-cards">
        <div class="col-12 col-md-4">
          <div class="card">
            <img src="../assets/materiale/images/foto-1.jpg" alt="">
           <p>
             I am free to learn at my own pace, follow my own schedule and choose the subkect I like. Great study portal for people like me.
           </p>
          <h5>MINA HOLLACE</h5>
          <div class="rule">
            / Freelancer
          </div>
          </div>
        </div>
        <div class="col-12 col-md-4">
          <div class="card">
            <img src="../assets/materiale/images/foto-2.jpg" alt="">
            <p>
              MaxCoach is my best choice. Their tutors are smart and professional whe dealing with students.
            </p>
            <h5>MADLEY PONDOR</h5>
            <div class="rule">
            / IT Specialist
            </div>
          </div>
        </div>
        <div class="col-12 col-md-4">
          <div class="card">
            <img src="../assets/materiale/images/foto-3.jpg" alt="">
            <p>I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.
            </p>
            <h5>LUVIC DUBBLE</h5>
            <div class="rule">
            / Private Tutor
          </div>
          </div>
        </div>
        <div class="col-12">
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle"></i>
          <i class="fas fa-circle"></i>
        </div>
      </div>
      <div class="row news">
        <div class="col-12">
          <p>Start today for getting <span>Online Certification</span></p>
          <h2>You can be your own guiding star with our help!</h2>
          <a href="#" class="btn btn-1">Get started now</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutUs',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/common.scss';
#about-us {
  background-color: var(--oneColor);
}
.title {
  text-align: center;
  margin: 3.125rem 0rem 1.875rem 0rem;
    p {
      @include p-top-title;
    }
    h3 {
      @include title-intro;
      margin-bottom: .625rem;
      span {
        @include span-title-intro;
      }
    }
}
.container-cards .col-12 {
  padding: .625rem;
  margin: 1.875rem 0rem;
}
.container-cards .col-12:last-child {
  i {
    margin: 0rem .3125rem;
  }
  text-align: center;
  margin-bottom: 1.875rem;
  margin-top: 0rem;
}
.card {
  text-align: center;
  position: relative;
  padding: 4.6875rem .625rem .9375rem .625rem;
  background-color: white;
  height: 100%;
  img {
    position: absolute;
    border-radius: 50%;
    width: 6.875rem;
    top: -3.125rem;
    left: calc(50% - 3.4375rem);
  }
  .rule,
  h5 {
    margin: .625rem 0rem;
  }
  .rule {
    font-size: .75rem;
  }
}
.news {
  position: relative;
  text-align: center;
  padding: 2.5rem 0rem;
  p {
    font-weight: bold;
    color: var(--fourColor);
    span {
      font-weight: normal;
      color: var(--threeColor);
    }
  }
  h2 {
    color: var(--fourColor);
    margin-bottom: 1.875rem;
  }
}

.news:after {
  content: "";
  background-image: url("../assets/materiale/images/linee.png");
  height: 6.25rem;
  width: 6.25rem;
  background-repeat: no-repeat;
  background-size: contain;
  position: absolute;
  top: calc(50% - 1.5625rem);
  left: .625rem;
}
.news:before {
  content: "";
  background-image: url("../assets/materiale/images/spin.png");
  height: 6.25rem;
  width: 6.25rem;
  background-repeat: no-repeat;
  background-size: contain;
  position: absolute;
  top: calc(70% - 3.125rem);
  right: .625rem;
}

@media screen and (max-width: 48rem){
  .news::after,
  .news::before {
    display: none;
  }
}
</style>
