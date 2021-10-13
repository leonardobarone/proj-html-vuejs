<template>
  <section id="counter">
    <div class="container">
      <div class="row">
        <div v-for="(dato, index) in dati" :key="index" class="col-6 col-md-3">
          <h3>{{dato.number}}</h3>
          <h6>{{dato.title.toUpperCase()}}</h6>          
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Counter',
  data() {
    return {
      dati: [
          {
          "title": "finished sessions",
          "number": "1.926"
          },
          {
          "title": "enrolled learnes",
          "number": "3.092+"
          },
          {
          "title": "online istructors",
          "number": "200"
          },
          {
          "title": "satisfaction rate",
          "number": "100%"
          },
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
#counter {
  background-color: var(--oneColor);
  margin: 1.25rem 0rem;
  padding: 1.875rem 0rem;
}

.col-6 {
  text-align: center;
  margin: .9375rem 0rem;
  h3 {
    font-size: 2.25rem;
    color: var(--threeColor);
  }
  h6 {
    letter-spacing: .125rem;
  }
}
</style>
