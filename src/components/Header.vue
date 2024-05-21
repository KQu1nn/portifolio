<script setup>
  import { ref, watchEffect } from 'vue';
  
  const navs = ref(["About","Experience", "Work", "Contact"]);
  const links = ref(["/","/experience","/work","/contact"]);
  const isVisible = ref(false);
  const toggle = ref(false);

  const openMenu = () => {
    isVisible.value = !isVisible.value;
    toggle.value = !toggle.value;
  }
  const closeBtn = ref('fa-solid fa-close fa-lg');
  const hamburgerBtn = ref('fa-solid fa-bars fa-lg');
  const currentBtn = ref(hamburgerBtn.value);

  const displayStyle = ref('none');

  watchEffect(() => {
    displayStyle.value = isVisible.value ? 'block' : 'none';
    currentBtn.value = toggle.value ? closeBtn.value : hamburgerBtn.value;
  });
</script>

<template>
  <!-- Menu Mobile -->
  <ul id="mobileMenu" :style="{ display: displayStyle }" >
    <hr />
      <li class="navMobile" v-for="(nav, index) in navs" :key="index">
        <div id="contentMobileMenu">
          <span id="countMenu">{{ index+1 }}.</span>
          <a v-bind:href="links[index]">{{ nav }}</a>
        </div>
        <hr />
      </li>
  </ul>
    
<div id="wrapper">
    <!-- Menu Desktop -->
    <p id="logo"><a href="/">dot</a></p>
    <ul id="menu">
      <li v-for="(nav, index) in navs" :key="index">
          <span id="countMenu">{{ index+1 }}.</span>
          <a v-bind:href="links[index]"id="navMenu">{{ nav }}</a>
      </li>
    <button>Resume</button>
    </ul>

  <!-- Open/Close Menu Mobile -->
    <span id="hamb" @click="openMenu">
      <i :class="currentBtn"
         style="color: #d9d9d9;"></i>
    </span>
</div>
</template>

<style scoped>
  #mobileMenu {
    position: absolute;
    width: 100%;
    height: 100%;
    background-color: #16194af4;

    border-top: solid 1px white;

    padding: 50px 0;
  }
.navMobile{
  display: flex;
  flex-direction: column;
  cursor: pointer;
  letter-spacing: 5px;
}
#contentMobileMenu {
  font-size: 20px;
  display: flex;
  justify-content: center;
}
hr {
  border: solid 1px #00ff6d63;;
  margin: 30px 0;
}
  #wrapper {
    width: 100%;
    height: 70px;

    padding: 0 35px;

    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  #logo {
    color: #57c586;
    font-size: 20px;
    font-weight: 600;
  }
  #navMenu {
    color: #e3e3e3;
  }
  #menu {
    display: flex;
    align-items: center;
    gap: 35px;
  }
  li {
    list-style: none;
    font-size: 12px;

    display: flex;
    flex-direction: row;
    gap: 5px;
  }
  #countMenu {
    font-weight: 600;
    color: #57c586;
  }
  button {
    padding: 5px 10px;
    background-color: transparent;
    color: #57c586;
    border: solid 1px #57c586;
    border-radius: 5px;
    cursor: pointer;
    transition: background-color 0.3s, color 0.3s;
  }
  button:hover {
  background-color: #57c586;
  font-weight: 600;
  color: #15173d;
}
#hamb {
  cursor: pointer;
  display: none;
}


@media screen and (max-width: 600px) {
  #menu {
    display: none;
    font-size: 25px;
  }
  #mobileMenu {
    padding: 70px 0;
  }
  
  #hamb {
    display: block;
    position: absolute;
    left: 90%;
  }
}
</style>
