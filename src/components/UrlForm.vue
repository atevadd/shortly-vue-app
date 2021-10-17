<template>
  <div class="shortener-wrapper">
    <div class="shortener">
      <form action="">
        <div class="input-box">
          <input
            type="url"
            name=""
            id="url-field"
            placeholder="Shorten a link here..."
            v-model="text"
            required
          />
          <small class="error">Please add a link</small>
        </div>
        <button @click="getInput" type="submit">Shorten it!</button>
      </form>
    </div>

    <div class="shortener-result-wrapper" v-if="links !== 0">
      <ShortenerResult v-for="link in links" :key="link.id" :link="link.original" :shortLink="shrtLink" cssClass="copied"/>
    </div>
  </div>
</template>

<script>
import ShortenerResult from "./ShortenerResult";

export default {
  name: "UrlForm",
  components:{
    ShortenerResult,
  },
  data(){
    return{
      text: "",
      originaLink: "",
      shrtLink: "",
      arrCounter: 0,
      links:[]
    }
  },
  methods: {
    getInput(e){
      e.preventDefault();
      fetch(`https://api.shrtco.de/v2/shorten?url=${this.text}`)
      .then(res => {
        return res.json();
      })
      .then(data =>{
        this.originaLink = data.result.original_link;
        this,this.shrtLink = data.result.full_short_link;
        this.links.push({
          id: this.arrCounter += 1,
          original: data.result.original_link,
          short: data.result.full_short_link,
        })
        console.log(this.links);
      })
      .catch(err => console.log(err))
    },
  }
};
</script>

<style scoped>
.shortener-wrapper {
  /* border: 1px solid green; */
  width: 80%;
  height: 120px;
  position: absolute;
  left: 50%;
  bottom: -60px;
  transform: translateX(-50%);
  z-index: 2;
}

.shortener-wrapper .shortener {
  width: 100%;
  height: 120px;
  background-color: var(--Dark-Violet);
  background-image: url("../assets/bg-shorten-desktop.svg");
  border-radius: 7px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.shortener form {
  width: 90%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.shortener form .input-box {
  position: relative;
  width: 80%;
  margin-right: 10px;
}
.shortener form input {
  display: block;
  width: 100%;
  height: 45px;
  border: none;
  outline: none;
  border-radius: 5px;
  /* margin-right: 10px; */
  padding: 0 15px;
  font-size: 0.89rem;
  font-family: inherit;
}
.shortener form input.invalid {
  border: 2px solid #ff5858;
}
.shortener form .input-box small {
  display: none;
  position: absolute;
  bottom: -23px;
  left: 0;
  color: #ff5858;
  font-weight: 500;
  font-style: italic;
}
.shortener form .input-box small.invalid {
  display: inline-block;
}
.shortener form button {
  padding: 12px 30px;
  background-color: var(--Cyan);
  color: #fff;
  font-family: inherit;
  font-weight: 500;
  border: none;
  outline: none;
  border-radius: 5px;
  cursor: pointer;
}

.shortener form button:hover {
  background-color: hsl(180, 68%, 43%);
}

.shortener-result-wrapper{
  width: 100%;
  margin-top: 30px;
}

</style>