<template>
  <div class="nav_links">
    <ul>
      <li>
        <a :href="obj.url" :class="{ active: obj.current }">{{ obj.text }}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "DropDownComponent",
  props: ["obj"],
};
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

.nav_links {
  ul {
    list-style: none;
    padding: 5px 1rem;

    li a {
      text-decoration: none;
      color: $black;
      text-transform: uppercase;

      &:hover {
        color: $blue;
      }
    }
  }
}
</style>
