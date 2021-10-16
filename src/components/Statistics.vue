<template>
  <section class="statistics">
    <div class="statistics-header">
      <h1>Advanced Statistics</h1>
      <p>
        Track how your links are performing across the web with our advanced
        statistics dashboard.
      </p>
    </div>

    <div class="statistics-cards">
      <div class="statistics-card">
        <div class="img">
          <img src="../assets/icon-brand-recognition.svg" alt="" />
        </div>
        <h2>Brand Recognition</h2>
        <p>
          Boost your brand recognition with each click. Generic links don’t mean
          a thing. Branded links help instil confidence in your content.
        </p>
      </div>
      <div class="statistics-card">
        <div class="img">
          <img src="../assets/icon-brand-recognition.svg" alt="" />
        </div>
        <h2>Detailed Records</h2>
        <p>
          Gain insights into who is clicking your links. Knowing when and where
          people engage with your content helps inform better decisions.
        </p>
      </div>
      <div class="statistics-card">
        <div class="img">
          <img src="../assets/icon-brand-recognition.svg" alt="" />
        </div>
        <h2>Fully Customizable</h2>
        <p>
          Improve brand awareness and content discoverability through
          customizable links, supercharging audience engagement.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Statistics",
};
</script>

<style scoped>
.statistics{
  width: 100%;
  height: 100vh;
  position: relative;
  background-color: #f4f4f4;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
}
.statistics .statistics-header{
  width: 30%;
  text-align: center;
}
.statistics .statistics-header h1{
  color: var(--Very-Dark-Violet);
  font-size: 1.9rem;
  margin-bottom: 10px;
}
.statistics .statistics-header p{
  color: var(--Grayish-Violet);
  font-size: .9rem;
}
.statistics .statistics-cards{
  position: relative;
  width: 80%;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  /* border: 1px solid; */
  margin-top: 35px;
  height: 40vh;
  z-index: 10;
}
.statistics .statistics-cards .statistics-card{
  position: relative;
  width: 30%;
  background-color: #fff;
  padding: 25px;
  border-radius: 5px;
  z-index: 10;
}
.statistics .statistics-cards .statistics-card:nth-child(1){
  align-self: flex-start;
}
.statistics .statistics-cards .statistics-card:nth-child(2){
  position: relative;
  align-self: center;
}
.statistics .statistics-cards .statistics-card:nth-child(2)::before{
  content: '';
  position: absolute;
  top: 30%;
  left: -90px;
  transform: translateY(-30%);
  width: 150px;
  height: 5px;
  background-color: var(--Cyan);
  z-index: -11001;
}
.statistics .statistics-cards .statistics-card:nth-child(3)::before{
  content: '';
  position: absolute;
  top: 30%;
  left: -90px;
  transform: translateY(-30%);
  width: 150px;
  height: 5px;
  background-color: var(--Cyan);
  z-index: 1;
}
.statistics .statistics-cards .statistics-card:nth-child(3){
  position: relative;
  align-self: flex-end;
}
.statistics-card h2{
  color: var(--Very-Dark-Violet);
  font-size: 1.2rem;
  margin-top: 25px;
  margin-bottom: 15px;
}
.statistics-card p{
  color: var(--Grayish-Violet);
  font-size: .85rem;
}
.statistics-card .img{
  position: absolute;
  top: -30px;
  background-color: var(--Dark-Violet);
  padding: 10px;
  border-radius: 50%;
  width: 60px;
  height: 60px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
}
.statistics-card .img img{
  width: 30px;
  height: 30px;
}
</style>