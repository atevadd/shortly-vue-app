<template>
  <NavBar />
  <Hero />
  <Statistics />
  <Banner />
  <Footer />
</template>

<script >
import NavBar from './components/NavBar';
import Hero from './components/Hero';
import Statistics from './components/Statistics';
import Banner from './components/Banner';
import Footer from "./components/Footer";

export default ({
  name: 'App',
  components: {
    NavBar,
    Hero,
    Statistics,
    Banner,
    Footer,
  }
});
</script>

<style>
:root {
  --Cyan: hsl(180, 66%, 49%);
  --Dark-Violet: hsl(257, 27%, 26%);
  --Red: hsl(0, 87%, 67%);

  --Gray: hsl(0, 0%, 75%);
  --Grayish-Violet: hsl(257, 7%, 63%);
  --Very-Dark-Blue: hsl(255, 11%, 22%);
  --Very-Dark-Violet: hsl(260, 8%, 14%);
}

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Poppins", sans-serif;
}

body {
  background: #fff;
  overflow-x: hidden;
}
</style>
