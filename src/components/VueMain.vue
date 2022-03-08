<template>
  <div class="container-fluid">
    <!-- first section  -->
    <section class="content-section">
      <div class="container">
        {{ text }}
      </div>
    </section>

    <!-- second section -->
    <section class="nav-section">
      <div class="container">
        <ul>
          <li v-for="(element, i) in menuLinks" :key="index">
            <figure>
              <img :src="require(`..assets${element.img}`)" alt="" />
            </figure>
            <a :href="element.href"> {{ element.text }} </a>
          </li>
        </ul>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "VueMain",

  data() {
    return {
      text: "<!-- content goes here -->",
      // array items menu link della nav-section
      menuLinks: [
        {
          img: "/img/buy-comics-digital-comics.png",
          href: "#",
          text: "DIGITAL COMICS",
        },
        {
          img: "/img/buy-comics-digital-comics.png",
          href: "#",
          text: "DIGITAL COMICS",
        },
        {
          img: "/img/buy-comics-digital-comics.png",
          href: "#",
          text: "DIGITAL COMICS",
        },
        {
          img: "/img/buy-comics-digital-comics.png",
          href: "#",
          text: "DIGITAL COMICS",
        },
        {
          img: "/img/buy-comics-digital-comics.png",
          href: "#",
          text: "DIGITAL COMICS",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.content-section {
  background-color: rgb(31, 31, 31);
  height: 100px;
  color: white;
  display: flex;
  align-items: center;
}

.nav-section {
  background-color: rgb(0, 132, 255);
  height: 160px;
}

.container {
  display: flex;
  align-items: center;
}
</style>