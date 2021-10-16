<template>
  <a href="#" class="btn">{{ content }}</a>
</template>

<script>
export default {
  name: "Button",
  props:{
    content: String,
  }
}
</script>

<style>
.btn{
  background-color: var(--Cyan);
  text-decoration: none;
  transition: .25s ease;
}
.btn:hover {
  background-color: hsl(180, 72%, 36%);
}
</style>