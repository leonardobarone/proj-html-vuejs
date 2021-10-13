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
  padding: 10px;
}

.card {
    border-radius: 5px;
    border: 1px solid black;
    overflow: hidden;
  .header-card{
    position: relative;
    img {
      width: 100%;
      display: block;
    }
    .price {
      position: absolute;
      border-radius: 0px 0px 0px 5px;
      background-color: var(--threeColor);
      color: white;
      font-size: 14px;
      padding: 5px 15px;
      top: 0px;
      right: 0px;
    }
  }
  .body-card {
    padding: 15px;
    .teacher {
      display: flex;
      align-items: center;
      img {
        border-radius: 50%;
        width: 25px;
      }
      h6 {
        margin-left: 10px;
        font-weight: normal;
        font-size: 12px;
      }
    }
    h3 {
      margin: 5px 0px;
      line-height: 24px;
    }
  }
}

.extra {
  display: flex;
  margin: 20px 0px 15px 0px;
  i {
    margin: 0px 10px;
  }
}

</style>
