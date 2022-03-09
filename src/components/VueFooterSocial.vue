<template>
  <div class="container-fluid">
    <div class="container">
      <div class="section">
        <button id="sign-up">sign-up now !</button>
      </div>

      <div class="section">
        <div id="follow-us">follow us</div>
        <ul class="social-icons">
          <li v-for="(el,i) in socialIcons" :key="i">
            <img :src="require(`../assets${el}`)" alt="" />
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VueFooterSocial",

  data(){
      return{
          socialIcons: ["/img/footer-facebook.png",
                        "/img/footer-twitter.png",
                        "/img/footer-youtube.png",
                        "/img/footer-pinterest.png",
                        "/img/footer-periscope.png"],
      }
  }
};
</script>

<style lang="scss" scoped>
.container-fluid {
  background-color: rgb(48, 48, 48);
}

.container {
  display: flex;
  align-items: center;
  height: 100px;

  .section {
    height: 100%;
    width: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  #sign-up {
    color: white;
    background-color: transparent;
    border: 2px solid rgb(0, 132, 255);
    padding: 10px;
    text-transform: uppercase;
    font-weight: 600;
    cursor: pointer;
    &:hover {
      box-shadow: inset 0px 0px 13px 1px rgba(255,255,255,0.57);
    }
  }

  #follow-us {
    color: rgb(0, 132, 255);
    text-transform: uppercase;
    font-weight: 700;
    padding: 0 30px;
  }

  .social-icons{
  display: flex;
  gap: 10px;
  }
}
</style>
