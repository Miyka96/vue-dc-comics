<template>
  <div class="container-fluid">
    <div class="container">
      <figure>
        <img src="../assets/img/dc-logo.png" alt="" />
      </figure>
      <div class="nav">
        <ul>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
          <li><a href="#"> list item </a></li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VueHeader",

  data() {
    return {
      text: "header here",
    };
  },
};
</script>

<style lang="scss" scoped>
.container {
  display: flex;
  align-items: center;
  height: 110px;
}

figure {
  width: 30%;
}

.nav {
  flex-grow: 1;
  height: 100%;
}

ul {
  display: flex;
  flex-wrap: nowrap;
  height: 100%;
  align-items: center;
  border-bottom: 4px solid white;

  li {
    padding: 0 12px;

    text-transform: capitalize;
    font-size: 12px;

    a {
        color: rgb(61, 61, 61);
        padding-bottom: 45px;
        padding-top: 40px;
        font-weight: 700;

      &:hover {
        border-bottom: 4px solid blue;
        color: blue;
      }
    }
  }
}
</style>