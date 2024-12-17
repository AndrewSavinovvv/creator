<script setup>

</script>

<template>
  <div class="trust container">
    <h1>Trusted by</h1>
    <div class="trust__block">
      <ul class="trust__block-list">
        <li>
          <img src="@/assets/img/mini-logo.png" alt="">
        </li>
        <li>
          <img src="@/assets/img/mini-logo.png" alt="">
        </li> <li>
        <img src="@/assets/img/mini-logo.png" alt="">
      </li> <li>
        <img src="@/assets/img/mini-logo.png" alt="">
      </li>
      </ul>
    </div>
  </div>
</template>

<style scoped>
.trust {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 125px;
}
.trust h1 {
  color: black;
  font-weight: 400;
  font-size: 18px;
  margin-bottom: 45px;
}
.trust__block-list {
  display: flex;
  gap: 100px;
}
</style>