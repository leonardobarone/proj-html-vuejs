<template>
  <section id="courses">
    <div class="container">
      <div class="row">
        <div class="col-12 title">
          <p>CHOSE WHERE YOU'D LIKE TO BEGIN</p>
          <h3>Latest Featured <span>Courses</span></h3>
        </div>
      </div>
     </div>
      
      <div class="container-fluid bg-color">
        <div class="container">
          <div class="row cards">
            <div v-for="(course, index) in courses" :key="index" class="col-12 col-md-4">
              <div class="card">
                <div class="header-card">
                  <img :src="require(`../assets/materiale/images/${course.imgCourse}`)" alt="">
                  <div class="price">{{course.price}}</div>                
                </div>
                <div class="body-card">
                  <div class="teacher">
                    <img :src="require(`../assets/materiale/images/${course.imgTeacher}`)" alt="">
                    <h6>{{course.nameTeacher}}</h6>
                  </div>
                  <h3>{{course.nameCourse}}</h3>
                  <div class="extra">
                    <div class="lessons">
                      <i class="far fa-file-alt"></i>
                      <span>{{course.lessons}} Lessons</span>
                    </div>
                    <div class="students">
                      <i class="far fa-user"></i>
                      <span>{{course.students}} Students</span>
                    </div>
                  </div>
                </div>
              </div> 
            </div>
          </div>
          <div class="row with-btn">
            <div class="col-12">
              <a href="#" class="btn btn-1">
                View all courses
                <i class="fas fa-long-arrow-alt-right"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
     
   
  </section>
</template>

<script>
import json from '../assets/script/courses.json';

export default {
  name: 'Courses',
  data() {
    return {
      courses: json,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/common.scss';

#courses {
  .title {
    text-align: center;
    margin: 2.5rem 0rem;
    p {
      @include p-top-title;
    }
    h3 {
      @include title-intro;
      span {
        @include span-title-intro;
      }
    }
  }
}



.bg-color {
  background-color: var(--oneColor);
}

.cards .col-12 {
  padding: .625rem;
}

.card {
    cursor: pointer;
    &:hover .body-card {
      background-color: white;
    }
    &:hover .header-card img {
      opacity: 1;
      // transition: 1s;
    }
    border-radius: .3125rem;
    // border: .0625rem solid black;
    overflow: hidden;
  .header-card{
    position: relative;
    img {
      width: 100%;
      opacity: 0.75;
      transition: opacity 1s ease-out;
      display: block;
    }
    .price {
      position: absolute;
      border-radius: 0rem 0rem 0rem .3125rem;
      background-color: var(--threeColor);
      color: white;
      font-size: .875rem;
      padding: .3125rem .9375rem;
      top: 0rem;
      right: 0rem;
    }
  }
  .body-card {
    transition: background-color 1s ease-out;
    padding: .9375rem;
    .teacher {
      display: flex;
      align-items: center;
      img {
        border-radius: 50%;
        width: 1.5625rem;
      }
      h6 {
        margin-left: .625rem;
        font-weight: normal;
        font-size: .75rem;
      }
    }
    h3 {
      margin: .3125rem 0rem;
      line-height: 1.5rem;
    }
  }
}

.extra {
  display: flex;
  margin: 1.25rem 0rem .9375rem 0rem;
  i {
    margin: 0rem .625rem;
  }
}
.with-btn {
  text-align: center;
  padding: .625rem 0rem 2.5rem 0rem;
  .btn i {
    margin-left: 0.5rem;
    vertical-align: middle;
  }
}

</style>
