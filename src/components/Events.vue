<template>
  <section id="events">
    <div class="container">
      <div class="row">
        <div class="col-12 title">
          <p>GET IN CONTACT NOW</p>
          <h3>Upcoming <span>Events</span></h3>
        </div>
      </div>
      <div class="row container-cards">
        <div v-for="(event, index) in events" :key="index" class="col-12 col-md-6">
          <div class="card">
            <div class="col-left">
              <div class="place">
                <i class="fas fa-map-marker-alt"></i>
                {{event.place}}
              </div>
              <h3>{{event.name}}</h3>
            </div>
            <div class="col-right">
              <div class="number">
                22
              </div>
              <div class="month">
                NOV
              </div>
              <a href="#" class="btn btn-1">Get ticket</a>
            </div>
          </div>
        </div>      
      </div>
      <div class="row events-bottom">
        <div class="col-12">
          <span>
            Excited about our event?
          </span>
            <a href="#" class="btn btn-3">View all events <i class="fas fa-long-arrow-alt-right"></i></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Events',
  data() {
    return {
      events: [
        {
        "place": "Texas, US",
        "name": "Storytelling Workshop",
        "day": "22",
        "month": "NOV",
        },
        {
        "place": "Hamburg, GermanyS",
        "name": "International Art Fair 2020",
        "day": "23",
        "month": "NOV",
        },
        {
        "place": "Illinois, US",
        "name": "Consumer Food Safety Education Conference",
        "day": "22",
        "month": "JUL",
        },
        {
        "place": "New York",
        "name": "Painting Art Contest 2020",
        "day": "10",
        "month": "OCT",
        },
        {
        "place": "Illinois, US",
        "name": "Street Performance: Call for Artis",
        "day": "15",
        "month": "DEC",
        },
        {
        "place": "Dubai",
        "name": "How meditation improve your mental health?",
        "day": "12",
        "month": "AUG",
        },
      ],
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/style/common.scss';
#events {
 .title {
   margin: 25px 0px;
   text-align: center;
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
}

.col-12 {
  padding: 10px;
}
.card {
  cursor: pointer;
  border-left: 4px solid transparent;
  transition: 1s;
  &:hover {
    box-shadow: 0px 2px 4px gray;
    .btn {
      background-color: var(--fourColor);
    }
    background-color: white;
    border-left: 4px solid var(--threeColor);
  }
  background-color: var(--oneColor);
  opacity: 0.8;
  padding: 20px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  .place {
    margin-bottom: 5px;
  }
  .number {
    font-size: 48px;
    color: var(--threeColor);
  }
  .month {
    font-weight: bold;
  }
  .col-right {
    width: 35%;
    text-align: center;
  }
  .col-left {
    width: 65%;
  }
}

.btn-3 {
  font-weight: bold;
  font-size: 20px;
  color: var(--threeColor);
  &:hover {
    background-color: var(--oneColor);
  }
  i {
    vertical-align: middle;
  }
}

.events-bottom {
  text-align: center;
  margin: 20px 0px 20px 0px;
  span {
  font-size: 20px;
}
}
</style>
