<template>
  <section class="banner">
    <h1>Boost your links today</h1>
    <Button content="Get Started"/>
  </section>
</template>

<script>
import Button from "./Button";

export default {
  name: "Banner",
  components:{
    Button,
  }
}
</script>

<style scoped>
.banner{
  width: 100%;
  height: 30vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: var(--Dark-Violet);
  background-image: url("../assets/bg-boost-desktop.svg");
}
.banner h1{
  font-size: 1.8rem;
  color: #fff;
  font-weight: 700;
  margin-bottom: 10px;
}
.banner .btn{
  display: block;
  padding: 12px 30px;
  border-radius: 50px;
  font-size: .9rem;
  font-weight: 500;
  color: #fff;
}
</style>