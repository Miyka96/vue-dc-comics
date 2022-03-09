<template>
  <div class="container-fluid">
    <div class="container">
      <figure>
        <img src="../assets/img/dc-logo.png" alt="" />
      </figure>
      <div class="nav">
        <ul>
          <li v-for="(el,i) in links" :key="i">
            <a :href="el.href" :class=" el.active ? 'active' : '' "> {{el.text}} </a>
          </li>
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
      links: [
        {
          text: "CHARACTERS",
          href: "#",
        },
        {
          text: "COMICS",
          href: "#",
          active: true,
        },
        {
          text: "MOVIES",
          href: "#",
        },
        {
          text: "TV",
          href: "#",
        },
        {
          text: "GAMES",
          href: "#",
        },
        {
          text: "COLLECTIBLES",
          href: "#",
        },
        {
          text: "VIDEOS",
          href: "#",
        },
        {
          text: "FANS",
          href: "#",
        },
        {
          text: "NEWS",
          href: "#",
        },
        {
          text: "SHOP",
          href: "#",
        },
      ],
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
  width: 20%;
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

      &:hover, &.active {
        border-bottom: 4px solid blue;
        color: blue;
      }
    }
  }
}
</style>
