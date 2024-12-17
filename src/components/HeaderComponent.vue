<script setup>
</script>

<template>
  <header class="container">
    <div class="header__logo">
      <img src="@/assets/img/logo.png" alt="Logo" />
    </div>
    <nav class="header__nav">
      <ul class="nav__nav__list">
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#blog">Blog</a></li>
        <li class="nav__nav__list-last">
          <a href="#call">
            <span>Book a call</span>
            <img src="@/assets/icon/arrow-right.svg" alt="Arrow" />
          </a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  padding-top: 40px;
  align-items: center;
}

.nav__nav__list {
  display: flex;
  gap: 40px;
  color: #000000;
}

.nav__nav__list li {
  font-size: 16px;
  font-weight: 400;
}

.nav__nav__list a {
  text-decoration: none;
  color: inherit;
}

.nav__nav__list-last span {
  margin-right: 8px;
}

.nav__nav__list-last {
  cursor: pointer;
  display: flex;
  align-items: center;
}
</style>