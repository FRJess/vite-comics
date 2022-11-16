<script>
export default {
  name: 'AppFooterTop',

}
</script>

<template>
  <footer>
    <div class="container">
      <div class="cols">
        <div class="links">
          <h4>DC Comics</h4>
          <nav>
            <ul>
              <li><a href="#">Characters</a></li>
              <li><a href="#">Comics</a></li>
              <li><a href="#">Movies</a></li>
              <li><a href="#">TV</a></li>
              <li><a href="#">Games</a></li>
              <li><a href="#">Videos</a></li>
              <li><a href="#">News</a></li>
            </ul>
          </nav>
        </div>
        <div class="links">
          <h4>Shop</h4>
          <nav>
            <ul>
              <li><a href="#">Shop DC</a></li>
              <li><a href="#">Shop DC Collectibles</a></li>
            </ul>
          </nav>
        </div>
      </div>
      <div class="cols">
        <div class="links">
          <h4>DC</h4>
          <nav>
            <ul>
              <li><a href="#">Terms of use</a></li>
              <li><a href="#">Privacy policy (New)</a></li>
              <li><a href="#">Ad Choices</a></li>
              <li><a href="#">Advertising</a></li>
              <li><a href="#">Jobs</a></li>
              <li><a href="#">Subscriptions</a></li>
              <li><a href="#">Talent Workshops</a></li>
              <li><a href="#">CPSC Certificates</a></li>
              <li><a href="#">Ratings</a></li>
              <li><a href="#">Shop Help</a></li>
              <li><a href="#">Contact Us</a></li>
            </ul>
          </nav>
        </div>
      </div>
      <div class="cols">
        <div class="links">
          <h4>Sites</h4>
          <nav>
            <ul>
              <li><a href="#">DC</a></li>
              <li><a href="#">MAD Magazine</a></li>
              <li><a href="#">DC Kids</a></li>
              <li><a href="#">DC Universe</a></li>
              <li><a href="#">DC Power Visa</a></li>
            </ul>
          </nav>
        </div>
      </div>
    </div>
    <img src="../assets/img/dc-logo-bg.png" alt="">
  </footer>
  
</template>

<style lang="scss" scoped>

@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

footer{
  display: flex;
  background-image: url('../assets/img/footer-bg.jpg');
  padding-top: 30px;
  // width: 50%;
  overflow-y:hidden;
  img{
    max-width: 30%;
    transform: translateY(-24%);
    margin-right: 200px;
  } 
  .container{
    display: flex;
    // display: flex;
    .cols{
      margin-left: 50px;
      h4{
      color: white;
      text-transform: uppercase;
      font-weight: 600;
      margin-bottom: 10px;
    }
      ul{
        list-style: none;
        padding-bottom: 20px;
        a{
          display: inline-block;
          text-decoration: none;
          color: #6B6558;
          font-size: .85em;
        }
      }
    }
  }
  
  
}

</style>