<template>
  <header class="container">
    <img src="../assets/img/dc-logo.png" alt="dc logo" />
    <nav>
      <ul class="nav_links">
        <li v-for="(item, index) in links" :key="index">
          <a :href="item.url" :class="{ active: item.current }">{{ item.text }}</a>
          <div class="underliner" :class="{ active: item.current }"></div>
        </li>
      </ul>
    </nav>
    <span @click="this.dropDown = !this.dropDown"><i class="fa-solid fa-bars"></i></span>
    <Transition name="slide-fade">
      <div class="dropdown_menu" v-if="dropDown">
        <DropDownComponent v-for="(item, index) in links" :key="index" :obj="item" />
      </div>
    </Transition>
  </header>
</template>

<script>
import { NavBarlinks } from "../data/datas.js";
import DropDownComponent from "./DropDownComponent.vue";
export default {
  name: "HeaderComponent",
  components: { DropDownComponent },
  data() {
    return {
      dropDown: false,
      links: NavBarlinks,
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

header {
  @include dflex;
  position: relative;

  img {
    width: 70px;
  }
  ul {
    @include dflex;
    list-style: none;

    li {
      position: relative;
    }

    li a {
      display: block;
      text-decoration: none;
      text-transform: uppercase;
      font-size: 0.7rem;
      padding: 1rem;
      font-weight: bold;
      color: $black;
      transition: all 0.3s ease;
      &:hover:not(.active) {
        color: gray;
      }
    }
  }
  span {
    font-size: 1.2rem;
    text-transform: uppercase;
    font-weight: bold;
    display: none;

    &:hover {
      cursor: pointer;
      color: $blue;
    }
  }
  .underliner {
    background-color: $blue;
    height: 5px;
    width: 60%;
    position: absolute;
    left: 20%;
    bottom: -1.8rem;
    opacity: 0;

    &.active {
      opacity: 1;
    }
  }
  .active {
    color: $blue;
  }

  .dropdown_menu {
    position: absolute;
    @include dflex-column;
    width: 100%;
    height: 320px;
    top: 6rem;
    left: 0;
    padding: 1rem 0;
    z-index: 1000;
    border-top: 1px solid gray;
    background-color: white;
  }

  @media screen and (max-width: 768px) {
    nav {
      display: none;
    }

    span {
      display: block;
      font-size: 2.5rem;
    }
  }
  .slide-fade-enter-active {
    transition: all 0.2s ease-out;
  }

  .slide-fade-leave-active {
    transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
  }

  .slide-fade-enter-from,
  .slide-fade-leave-to {
    transform: translateY(-20px);
    opacity: 0;
  }
}
</style>
