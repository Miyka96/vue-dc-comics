<template>
  <div class="container-fluid">
    <div class="container">
      <ul>
        <li v-for="(element, i) in footerLinks" :key="i">
          <div id="title">{{ element.title }}</div>
          <div id="list-items" v-for="(el, i) in element.list" :key="i">
            {{ el }}
          </div>
        </li>
      </ul>

      <figure>
        <img src="" alt="">
      </figure>
    </div>
  </div>
</template>

<script>
export default {
  name: "VueFooter",

  data() {
    return {
      text: "main here",
      footerLinks: [
        {
          title: "DC COMICS",
          list: ["Characters", "Comics", "Tv", "Games", "Videos", "News"],
        },
        {
          title: "DC",
          list: [
            "Terms Of Use",
            "Privacy policy (New)",
            "Ad Choices",
            "Advertising",
            "Jobs",
            "Subscriptions",
            "Talent Workshops",
            "CPSC Certificates",
            "Ratings",
            "Shop Help",
            "Contact Us",
          ],
        },
        {
          title: "SITES",
          list: [
            "DC",
            "MAD Magazine",
            "DC Kids",
            "DC Universe",
            "DC Power Visa",
          ],
        },
        {
          title: "SHOP",
          list: ["Shop DC", "Shop DC Collectibles"],
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.container-fluid {
  min-height: 300px;
  background-image: url("../assets/img/footer-bg.jpg");
}

ul {
  display: flex;
  width: 45%;
  flex-wrap: wrap;
  color: white;
  padding: 30px 0;

  li {
    padding: 0 25px;
  }
}

#title {
    font-size: 20px;
    padding-bottom: 3px;
}

#list-items{
    font-size: 12px;
    color: grey;
    cursor: pointer;
    padding: 3px 0;

    &:hover{
        color: white;
    }
}
</style>
