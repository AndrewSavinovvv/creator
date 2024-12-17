<script setup>
import { ref, computed } from "vue";
import img from "@/assets/img/pr.png";
import icon from "@/assets/icon/arrow-right.svg";
import img2 from "@/assets/img/2.png";

const projects = [
  {
    id: 1,
    category: "Branding",
    title: "Soulful Rebrand",
    image: img,
    icon: icon,
  },
  {
    id: 2,
    category: "Branding",
    title: "Creative Work",
    image: img2,
    icon: icon,
  },
  {
    id: 3,
    category: "Branding",
    title: "Design Excellence",
    image: img,
    icon: icon,
  },
];

const sliderActive = ref(0);

const nextSlide = () => {
  if (sliderActive.value < projects.length - 1) {
    sliderActive.value += 1;
  } else {
    sliderActive.value = 0;
  }
};

const prevSlide = () => {
  if (sliderActive.value > 0) {
    sliderActive.value -= 1;
  } else {
    sliderActive.value = projects.length - 1;
  }
};

const visibleProjects = computed(() => {
  return projects.slice(sliderActive.value, sliderActive.value + 3);
});
</script>

<template>
  <div class="projects container">
    <h4>PROJECTS</h4>
    <div class="projects__header">
      <h1>
        I bring results. <br />
        My clients are proof.
      </h1>
      <button>View all projects</button>
    </div>
    <div class="projects__list">
      <div
          v-for="project in visibleProjects"
          :key="project.id"
          class="projects__list-item"
      >
        <img :src="project.image" alt="Project Image" />
        <div class="projects__list-item-details">
          <h6>{{ project.category }}</h6>
          <h5>{{ project.title }}</h5>
          <button>
            <span>View Project</span>
            <img :src="project.icon" alt="Arrow Icon" />
          </button>
        </div>
      </div>
    </div>
    <div class="slider__btn">
      <div class="slider__btns">
        <button @click="prevSlide">
          <img src="@/assets/icon/slider-left.svg" alt="Prev" />
        </button>
        <button @click="nextSlide">
          <img src="@/assets/icon/slider-right.svg" alt="Next" />
        </button>
      </div>
    </div>
  </div>
</template>
<style scoped>
.projects__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 16px;
}
.projects {
  padding-top: 76px;
  position: relative;
  top: 280px;
}
.projects h4 {
  color: #b16cea;
  font-weight: 700;
  font-size: 22px;
  line-height: 22px;
  letter-spacing: 4px;
}
.projects__header h1 {
  color: black;
  font-size: 54px;
  font-weight: 700;
  line-height: 59px;
  letter-spacing: 1px;
}
.projects__header button {
  background: black;
  border: none;
  width: 201px;
  height: 58px;
  color: white;
  font-weight: 400;
  font-size: 18px;
  line-height: 18px;
  cursor: pointer;
}
.projects__list {
  display: flex;
  margin-top: 65px;
  gap: 24px;
}
.projects__list-item {
  display: flex;
  flex-direction: column;
  background: white;
  padding-bottom: 36px;
}
.projects__list-item-details {
  padding-left: 32px;
  padding-top: 33px;
}
.projects__list-item-details h5 {
  color: black;
  font-weight: 700;
  font-size: 24px;
  line-height: 26px;
  margin-top: 15px;
}
.projects__list-item h6 {
  color: #3c46ff;
  font-size: 14px;
  font-weight: 700;
  line-height: 14px;
  letter-spacing: 4px;

}
.projects__list-item-details button {
  margin-top: 22px;
  background: none;
  cursor: pointer;
  border: none;
  font-weight: 400;
  font-size: 18px;
  line-height: 18px;
}
.projects__list-item-details button span {
  margin-right: 10px;
}
.slider__btn {
  display: flex;
  justify-content: flex-end;
  margin-top: 59px;
}
.slider__btn img {
  height: 14px;
  width: 10px;
}
.slider__btn  button{
  padding: 21px;
  cursor: pointer;
  border: none;
  margin-right: 7px;
  background: white;
  width: 54px;
  height: 54px;
}
</style>