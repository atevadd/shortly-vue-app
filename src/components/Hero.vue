<template>
  <section class="hero">
    <div class="container">
      <div class="hero-text">
        <h1>More than just shorter links</h1>
        <p>
          Build your brand’s recognition and get detailed insights on how your
          links are performing.
        </p>
        <Button content="Get started" />
      </div>
      <div class="hero-image">
        <img src="../assets/illustration-working.svg" alt="" />
      </div>
    </div>
    <UrlForm />
  </section>
</template>

<script>
import Button from "./Button";
import UrlForm from "./UrlForm";

export default {
  name: "Hero",
  components: {
    Button,
    UrlForm,
  },
};
</script>

<style scoped>
.hero {
  width: 100%;
  height: 70vh;
  position: relative;
  /* border: 1px solid; */
}
.container {
  position: relative;
  width: 80%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin: 0 auto;
}
.hero-text {
  width: 55%;
  /* border: 1px solid red; */
}
.hero-text h1 {
  font-size: 3.8rem;
  line-height: 1.2;
  color: var(--Very-Dark-Violet);
}
.hero-text p {
  padding-right: 100px;
  color: var(--Grayish-Violet);
}
.hero-text .btn {
  text-decoration: none;
  display: block;
  width: max-content;
  margin-top: 40px;
  padding: 12px 30px;
  border-radius: 50px;
  font-weight: 500;
  color: #fff;
  font-size: 0.9rem;
}
button:hover {
  background-color: hsl(180, 68%, 43%);
}
.hero-image {
  width: 70%;
  height: 100%;
  /* border: 1px solid red; */
  transform: translateX(220px);
  /* position: absolute;
  right: 0;
  top: 0; */
}
.hero-image img {
  width: 100%;
  height: 100%;
}
</style>