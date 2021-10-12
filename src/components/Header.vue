<template>
  <header>
    <div class="container">
      <div class="row align-items-center">
        <div class="col-3 col-left">
          <a href="#">
            <img class="title-header" src="../assets/materiale/images/dark-logo.png" alt="logo max coach">
          </a>
        </div>
        <div class="col-9 col-right">
          <nav>
            <ul>
              <li>
                <a href="#">
                  Home
                </a>
              </li>
              <li>
                <a href="#">
                  Pages
                </a>
              </li>
              <li>
                <a href="#">
                  Courses
                </a>
              </li>
              <li>
                <a href="#">
                  Features
                </a>
              </li>
              <li>
                <a href="#">
                  Blog
                </a>
              </li>
              <li>
                <a href="#">
                  Shop
                </a>
              </li>
            </ul>
          </nav>
          <div class="account">
               <a href="#">
                <img class="cart" src="../assets/materiale/shopping-cart.png" alt="logo cart">
                <div class="zero">0</div>
              </a>
              <a href="#">
                <i class="far fa-user-circle"></i>
              </a>
          </div>
          <input class="wrapper" type="text" placeholder="Search...">
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

header {
  background-color: var(--oneColor);
  padding: .9375rem;
}

.title-header {
  width: 8.75rem;
  display: block;
}

.col-right {
  justify-content: right;
  display: flex;
  align-items: center;
}

nav ul {
  display: flex;
  li {
    margin: 0rem .625rem;
    a {
      color: var(--twoColor);
      font-size: .875rem;
      &::after {
        content: "\f078";
        font-weight: bold;
        font-family: "Font Awesome 5 Free";
        vertical-align: middle;
        font-size: .625rem;
        display: inline-block;
      }
    }
  }
}

.cart {
    width: 15px;
}

.account i {
  color: var(--twoColor);
  margin: 0px 10px 0px 10px;
}

.account a:first-child {
  position: relative;
}

.zero {
  text-align: center;
  font-size: 6px;
  line-height: 11px;
  height: 11px;
  width: 11px;
  background-color: var(--threeColor);
  color: white;
  position: absolute;
  border-radius: 50%;
  top: -2px;
  right: -4px;
}


input {
  font-family: 'Poppins', sans-serif;
  padding: 7px 14px;
  border-style: none;
  background-image: url('../assets/materiale/search.png');
  background-repeat: no-repeat;
  background-size: 14px;
  background-position: right;
  background-origin: content-box;
}

</style>
