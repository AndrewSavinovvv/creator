<script setup>
const blogItems = Array(5).fill({
  date: "April 16, 2021",
  time: "6 mins",
  title: "Design tips for designers, that cover everything you need",
});
</script>

<template>
  <div class="blogs__wrapper">
    <div class="blogs container">
      <div class="blogs__left">
        <h6>BLOGS</h6>
        <h1>Latest Blogs</h1>
        <button class="blogs__left-btn">
          <span>View all</span>
          <img src="@/assets/icon/white-arrow.svg" alt="" />
        </button>
      </div>
      <div class="blogs__right">
        <div v-for="(item, index) in blogItems" :key="index" class="blogs__right-item">
          <div class="blogs__right-item__time">
            <div>
              {{ item.date }}
              <img src="@/assets/icon/cude-white.svg" alt="" />
              {{ item.time }}
            </div>
          </div>
          <p>{{ item.title }}</p>
          <button class="blogs__right-item__btn">
            <span>Read the article</span>
            <img src="@/assets/icon/white-arrow.svg" alt="" />
          </button>
          <div class="blogs__right-item__line"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.blogs {
  display: flex;
  gap: 72px;
  padding-top: 350px;
}
.blogs__wrapper {
  background: black;
}
.blogs__left {
  width: 449px;
}
.blogs__left h6 {
  color: #FFA84B;
  font-weight: 700;
  font-size: 22px;
  line-height: 22px;
  letter-spacing: 4px;
}
.blogs__left h1 {
  color: white;
  font-size: 54px;
  font-weight: 700;
  line-height: 59px;
  letter-spacing: 1px;
  margin-top: 16px;
}
.blogs__left-btn {
  margin-top: 35px;
  background: none;
  color: white;
  border: none;
  cursor: pointer;
}
.blogs__left-btn span {
  font-weight: 700;
  font-size: 18px;
  line-height: 18px;
  margin-right: 20px;
}
.blogs__right {
  width: 50%;
}
.blogs__right-item__time {
  color: #FFFFFFB2;
  font-size: 15px;
  font-weight: 700;
  line-height: 15px;
}
.blogs__right-item__time img {
  margin-right: 3px;
}
.blogs__right-item p {
  color: white;
  margin-top: 23px;
  font-weight: 700;
  font-size: 28px;
  line-height: 36px;
  width: 489px;
}
.blogs__right-item__btn {
  background: none;
  border: none;
  cursor: pointer;
  font-size: 18px;
  font-weight: 700;
  line-height: 18px;
  color: white;
  margin-top: 39px;
  padding: 0;
}
.blogs__right-item__btn span {
  margin-right: 19px;
}
.blogs__right-item__line {
  height: 1px;
  width: 100%;
  background: #FFFFFF4D;
  margin-top: 39px;
  margin-bottom: 65px;
}
</style>