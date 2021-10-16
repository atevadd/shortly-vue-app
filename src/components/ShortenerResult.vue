<template>
  <div class="shortener-result">
    <div class="links">
      <p class="search">{{ link }}</p>
      <p class="result">{{ shortLink }}</p>
    </div>
    <button @click="changeText" :class="cssClass" type="text">Copy</button>
  </div>
</template>

<script>
export default {
  name: "ShortenerResult",
  props: {
    link: String,
    shortLink: String,
    cssClass: String,
  },
  data(){
    return{
      isClicked: true,
    }
  },
  methods:{
    changeText(event){
      event.target.innerText = "Copied!";
    }
  },
};
</script>

<style scoped>
.shortener-result-wrapper .shortener-result{
  display: flex;
  align-items: center;
  background-color: #fff;
  padding: 20px;
  border-radius: 5px;
  box-shadow: 0 3px 13px rgba(0, 0, 0, .25);
  margin-bottom: 15px;
}
.shortener-result-wrapper .shortener-result .links{
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 90%;
}
.shortener-result-wrapper .shortener-result .links p{
  font-size: .88rem;
  color: #333;
  font-weight: 500;
}
.shortener-result-wrapper .shortener-result .links p.result{
  color: var(--Cyan);
  margin-right: 10px;
}
.shortener-result-wrapper .shortener-result button{
  width: 10%;
  padding: 8px;
  font-family: inherit;
  background-color: var(--Cyan);
  color: #fff;
  outline: none;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
.shortener-result-wrapper .shortener-result button:hover{
  background-color: hsl(180, 68%, 43%);
}
.shortener-result-wrapper .shortener-result button.copied{
  background-color: var(--Dark-Violet);
}
</style>