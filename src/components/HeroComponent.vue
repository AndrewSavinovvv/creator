<script setup>

</script>

<template>
  <div class="hero container">
    <div class="hero__left">
      <div class="hero__left-title">
        <h1>I design products</h1>
        <h2>that delight and inspire people.</h2>
      </div>
      <p>Hi! I’m Jake, a product designer based in Berlin. I create <br> user-friendly interfaces for fast-growing startups.</p>
     <div class="hero__left-btns">
       <button class="hero__left-btns-first">Book a call</button>
       <button class="hero__left-btns-second">
         <span>Download CV</span>
         <img src="@/assets/icon/arrow-right.svg" alt="">
       </button>
     </div>
    </div>
    <div class="hero__right">
      <img src="@/assets/img/IMAGE.png" alt="">
    </div>
  </div>
</template>

<style scoped>
.hero {
  display: flex;
  padding-top: 70px;
}
.hero__left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding-top: 55px;
}
.hero__left-title h1 {
  color: #FF8A56;
  font-size: 72px;
  font-weight: 700;
  line-height: 82px;
}
.hero__left-title h2 {
  font-size: 72px;
  font-weight: 700;
  line-height: 82px;
}
.hero__left p {
  color: #666666;
  font-weight: 400;
  font-size: 22px;
  line-height: 33px;
}
.hero__left-btns-first {
  background: black;
  border: none;
  height: 58px;
  width: 151px;
  color: white;
  font-size: 18px;
  font-weight: 400;
  cursor: pointer;
}
.hero__left-btns-second {
  background: none;
  height: 58px;
  border: none;
  font-size: 18px;
  font-weight: 400;
  text-align: center;
  cursor: pointer;
}
.hero__left-btns-second span {
  margin-right: 14px;
  margin-left: 40px;
}
</style>