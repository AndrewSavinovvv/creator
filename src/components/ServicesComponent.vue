<script setup>
import img from "@/assets/img/service.png";
import icon from "@/assets/icon/cube.svg";

const items = [
  {
    img: img,
    title: "What I can do for you",
    description: `Faster, better products that your<br>
                users love. Here's all the services I<br>
                provide:`,
    benefits: [
      { icon: icon, text: "Design Strategy" },
      { icon: icon, text: "Web and Mobile App Design" },
      { icon: icon, text: "Front-end Development" },
    ],
  },
  {
    img: img,
    title: "What I can do for you",
    description: `Faster, better products that your<br>
                users love. Here's all the services I<br>
                provide:`,
    benefits: [
      { icon: icon, text: "Design Strategy" },
      { icon: icon, text: "Web and Mobile App Design" },
      { icon: icon, text: "Front-end Development" },
    ],
  },
  {
    img: img,
    title: "What I can do for you",
    description: `Faster, better products that your<br>
                users love. Here's all the services I<br>
                provide:`,
    benefits: [
      { icon: icon, text: "Design Strategy" },
      { icon: icon, text: "Web and Mobile App Design" },
      { icon: icon, text: "Front-end Development" },
    ],
  },
];
</script>

<template>
  <div class="service container">
    <h4>Services</h4>
    <h1>Design that solves problems, <br> one product at a time.</h1>
    <div class="service__list">
      <div v-for="(item, index) in items" :key="index" class="service__list-item">
        <img :src="item.img" alt="" />
        <h5>{{ item.title }}</h5>
        <p v-html="item.description"></p>
        <ul class="service__list-benefisiar">
          <li v-for="(benefit, i) in item.benefits" :key="i">
            <img :src="benefit.icon" alt="" />
            <span>{{ benefit.text }}</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
.service {
  padding-top: 140px;
  text-align: center;
}
.service h4 {
  color: #FF5E69;
  font-size: 22px;
  font-weight: 700;
  line-height: 22px;
  text-transform: uppercase;
  letter-spacing: 4px;
  margin-bottom: 20px;
}
.service h1 {
  color: black;
  font-size: 54px;
  font-weight: 700;
  line-height: 59px;
  letter-spacing: 1px;
}
.service__list {
  display: flex;
  margin-top: 114px;
  gap: 90px;
  justify-content: space-between;
}
.service__list-item {
  display: flex;
  flex-direction: column;
  align-items: start;
}
.service__list-item img {
  height: 70px;
  width: 70px;
}
.service__list-item h5 {
  color: black;
  font-size: 24px;
  font-weight: 700;
  line-height: 26px;
  margin-top: 39px;
}
.service__list-item p {
  color: #666666;
  font-weight: 400;
  font-size: 16px;
  line-height: 28px;
  margin-top: 25px;
  text-align: left;
}
.service__list-benefisiar li img {
  height: 7px;
  width: 7px;
}
.service__list-benefisiar {
  display: flex;
  flex-direction: column;
  align-items: start;
  gap: 10px;
  margin-top: 21px;
}
.service__list-benefisiar li{
  display: flex;
  align-items: center;
  gap: 10px;
  font-size: 16px;
  font-weight: 700;
  line-height: 28px;
}
</style>