<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-logo">
        <a href="#">Shortly</a>
      </div>
      <div class="footer-links">
        <div class="column">
          <h1>Features</h1>
          <a href="#">Link Shortening</a>
          <a href="#">Branded Links</a>
          <a href="#">Analytics</a>
        </div>
        <div class="column">
          <h1>Resources</h1>
          <a href="#">Blog</a>
          <a href="#">Developers</a>
          <a href="#">Support</a>
        </div>
        <div class="column">
          <h1>Company</h1>
          <a href="#">About</a>
          <a href="#">Our Team</a>
          <a href="#">Careers</a>
          <a href="#">Contact</a>
        </div>
      </div>
      <div class="footer-socials">
        <ul>
          <li><a href="#"><i class="bx bx-facebook"></i></a></li>
          <li><a href="#"></a></li>
          <li><a href="#"></a></li>
          <li><a href="#"></a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style>
.footer{
  width: 100%;
  height: 50vh;
  background-color: var(--Very-Dark-Violet);
  display: flex;
  align-items: center;
  justify-content: center;
}
.footer .container{
  width: 80%;
  /* border: 1px solid #fff; */
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}
.footer-logo a{
  font-size: 1.7rem;
  color: #fff;
  text-decoration: none;
  font-weight: 600;
}
.footer-links{
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}
.footer-links .column{
  margin: 0 25px;
}
.footer-links .column a, .footer-links .column h1{
  display: block;
}
.footer-links .column h1{
  color: #fff;
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 15px;
}
.footer-links .column a{
  font-size: .8rem;
  margin-bottom: 15px;
  text-decoration: none;
  color: var(--Grayish-Violet);
}
.footer-socials ul{
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  list-style-type: none;
}
</style>