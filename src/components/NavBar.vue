<template>
  <header>
    <div class="container">
      <div class="brand-logo">
        <a href="#">Shortly</a>
      </div>
      <nav>
        <ul>
          <li><a href="#">Features</a></li>
          <li><a href="#">Pricing</a></li>
          <li><a href="#">Resources</a></li>
          <li><a href="#" class="log-btn">Login</a></li>
          <li><a href="#" class="sign-btn">Signup</a></li>
        </ul>
      </nav>
      <span class="ham"><i class="bx bx-menu"></i></span>
    </div>
  </header>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
header {
  width: 100%;
  position: relative;
  padding: 30px 0;
  /* border: 1px solid ; */
}
.container {
  width: 80%;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex: 1 1 0;
  flex-wrap: nowrap;
}
.brand-logo {
  position: relative;
  font-size: 1.7rem;
}
.brand-logo a {
  color: var(--Very-Dark-Blue);
  text-decoration: none;
  font-weight: 700;
  font-size: inherit;
}
nav{
  width: 100%;
  display: block;
}
nav ul{
  width: 100%;
  display: flex;
  align-items: center;
  flex: 1 1 0;
  flex-wrap: nowrap;
  list-style-type: none;
}
nav ul li{
  margin: 0 15px;
  display: inline-block;
}
nav ul li:nth-child(4){
  margin-left:  auto;
}
nav ul li a{
  text-decoration: none;
  color: var(--Grayish-Violet);
  font-size: .8rem;
  font-weight: 700;
}
nav ul li a.log-btn{
  margin: 0 auto;
}
nav ul li a.sign-btn{
  display: block;
  background-color: var(--Cyan);
  color: #fff;
  padding: 10px 15px;
  border-radius: 50px;
  transition: .25s ease;
}
nav ul li a.sign-btn:hover {
  background-color: hsl(180, 72%, 36%);
}
.ham{
  display: none;
}
</style>