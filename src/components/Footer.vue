<template>
  <footer>
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-6">
          <h3>Address</h3>
          <ul class="contacts">
            <li>382 NE 191st St # 87394 Miami, FL 33179-3899</li>
            <li>+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</li>
            <li>support@maxcocach.com</li>
          </ul>
          <ul class="social">
            <li>
              <i class="fab fa-facebook-square"></i>
            </li>
            <li>
              <i class="fab fa-twitter"></i>
            </li>
            <li>
              <i class="fab fa-instagram"></i>
            </li>
            <li>
              <i class="fab fa-linkedin"></i>
            </li>
          </ul>
        </div>
        <div class="col-12 col-md-4">
          <h3>Explore</h3>
          <ul class="explore">
            <li>Start here</li>
            <li>Blog</li>
            <li>About us</li>
            <li>Success story</li>
            <li>Courses</li>
            <li>Contact us</li>
          </ul>
        </div>
        <div class="col-12 col-md-2">
          <h3>Information</h3>
          <ul class="info">
            <li>Membership</li>
            <li>Purchase guide</li>
            <li>Privacy policy</li>
            <li>Terms of services</li>
          </ul>
        </div>
        <div class="col-12 footer-bottom">
          &#xa9; 2020 Maxcoach. All Rights Reserved
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
footer {
  padding: 2.3437rem 0rem;
}

.col-12 {
  padding: .9375rem;
}

@media screen and (max-width: 48rem){
  .col-12 {
    text-align: center;
  }
  .social {
    justify-content: center;
  }
  .explore li {
    width: 100% !important;
  }

}

.contacts {
  li {
    margin: .3125rem 0rem;
  }
}
  .social {
    display: flex;
    margin: 2.1875rem 0rem 0rem 0rem;
    li {
      i {
        margin-right: 2.0625rem;
        color: gray;
        font-size: 2.5rem;
      }
    }
    li:last-child i {
      margin-right: 0rem;
    }
  }

  .explore {
    display: flex;
    flex-wrap: wrap;
    li {
      width: 50%;
      margin: .3125rem 0rem;
    }
  }
  .info {
    li {
      margin: .3125rem 0rem;
    }
  }

  .footer-bottom {
    text-align: center;
  }
</style>
