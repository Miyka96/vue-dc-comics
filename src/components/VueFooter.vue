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

      <figure></figure>
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
  background-repeat: no-repeat;
  background-size: cover;
}

.container{
  display: flex;
  height: 500px;
}

ul {
  display: flex;
  width: 45%;
  flex-wrap: wrap;
  color: white;
  padding: 30px 0;

  li {
    padding: 0 30px;
  }
}

#title {
    font-size: 25px;
    padding-bottom: 3px;
}

#list-items{
    color: grey;
    cursor: pointer;
    padding: 3px 0;

    &:hover{
        color: white;
    }
}

figure{
  background-image: url("../assets/img/dc-logo-bg.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  height: 100%;
  width: 55%;
}
</style>
