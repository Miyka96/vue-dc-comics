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
          <li v-for="(el, i) in menuLinks" :key="i">
            <figure>
              <img :src="require(`../assets${el.img}`)" alt="" />
            </figure>
            <a :href="el.href"> {{ el.text }} </a>
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
          img: "/img/buy-comics-merchandise.png",
          href: "#",
          text: "DC MERCHANDISE",
        },
        {
          img: "/img/buy-comics-subscriptions.png",
          href: "#",
          text: "SUBSCRIPTION",
        },
        {
          img: "/img/buy-comics-shop-locator.png",
          href: "#",
          text: "COMIC SHOP LOCATOR",
        },
        {
          img: "/img/buy-dc-power-visa.svg",
          href: "#",
          text: "DC POWER VISA",
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
  display: flex;
  align-items: center;
  color: white;
}

.container {
  display: flex;
  align-items: center;
}

ul{
display: contents;

  li{
    flex-basis: 0;
    flex-grow: 1;
    display: flex;
    align-items: center;
    gap: 10px;
    height:60px;
      
      img{
        height: 100%;
      }  
      figure{
        display: contents;
      }
  }
}
</style>
