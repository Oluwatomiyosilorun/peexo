<template>
  <div class="home">
    <Navbar />
    <section>
      <div class="background_image mx-5 mt-3"></div>
      <div class="card_nav container p-0">
        <div class="show_card d-flex">
          <img
            src="https://www.bellanaija.com/wp-content/uploads/2020/07/Beverly-Naya-4.jpeg"
          />
          <button class="show_card_button" v-on:click="isHidden = !isHidden">
            Show card
          </button>
          <div class="profile" v-if="isHidden">
            <p
              v-on:click="isHidden = !isHidden"
              class="text-right p-2 mb-0 close"
            >
              Hide
            </p>
            <div class="modal-body mt-4">
              <img
                src="https://www.bellanaija.com/wp-content/uploads/2020/07/Beverly-Naya-4.jpeg"
              />
              <h4>Ekemini Mark</h4>
              <p>
                I’m a wedding and portrait photographer based in Lagos, Nigeria.
                I’ve been shooting weddings since I was in high school (before I
                ever had my driver’s license!).
              </p>
              <div class="d-flex justify-content-between">
                <div>
                  <h4 class="label">22.1k</h4>
                  <p class="total">Total View</p>
                </div>
                <div>
                  <h4 class="label">13.1k</h4>
                  <p class="total">Total Likes</p>
                </div>
                <div>
                  <h4 class="label">Sony 92J</h4>
                  <p class="total">Camera Lens</p>
                </div>
              </div>
              <div class="options">
                <div class="d-flex">
                  <p class="total">Category:</p>
                  <div class="d-flex justify-content-between">
                    <li>Food</li>
                    <li>Portrait</li>
                    <li>Wedding</li>
                    <li>Model</li>
                  </div>
                </div>

                <div class="d-flex">
                  <p class="total mb-0">Location:</p>
                  <p class="location mb-0">Lagos, Nigeria</p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <Portfolio />

        <!-- <div class="mini_nav">
                <p>Portfolio</p>
                <p>Availablity</p>
                <p>Pricing Package</p>
            </div> -->
      </div>
    </section>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import Portfolio from "@/components/Portfolio.vue";

export default {
  name: "Home",
  components: {
    Navbar,
    // ProfileModal,
    Portfolio,
  },
  data() {
    return {
      isHidden: true,
      fullWidthImage: false,
    };
  },
};
</script>

<style lang="scss" scoped>
.show_card {
  img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
  }
  .show_card_button {
    border: 0;
    background-color: inherit;
    margin-left: 10px;
    outline: none;
    box-shadow: none;
    cursor: pointer;
  }
}
.background_image {
  background-image: url("https://images.squarespace-cdn.com/content/v1/558c4c63e4b007dc3bfd0ea7/1435331722460-BW3DGIS7CG2BTS59KD4Y/ke17ZwdGBToddI8pDm48kAvDhARXUvFV7ncWLfoOlHhZw-zPPgdn4jUwVcJE1ZvWQUxwkmyExglNqGp0IvTJZamWLI2zvYWH8K3-s_4yszcp2ryTI0HqTOaaUohrI8PISaawsAQrbelz66K6MCrUR5w11wp2VM3_iFI5wf0NTmEKMshLAGzx4R3EDFOm1kBS/gallery-large_food_cod.jpg");
  background-position: inherit;
  background-size: cover;
  height: 165px;
  background-repeat: no-repeat;
  border-radius: 10px;
}

.profile {
  position: absolute;
  margin-top: -5%;
  width: 416px;
  background: white;
  border-radius: 10px;
  border: 0.25px solid #ffb500;
  border-radius: 4px;
  opacity: 1;
  .close {
    color: #e39400;
    font: normal bold normal 16px/21px Poppins;
  }
  .modal-body {
    padding: 2rem;
    img {
      width: 100px;
      height: 100px;
    }
    h4 {
      font: normal normal 600 30px/51px Poppins;
      color: #000000;
      opacity: 1;
    }
    p {
      font: normal normal normal 16px/25px Poppins;
      color: #000000;
    }
    .label {
      text-align: left;
      font: normal normal 600 18px/27px Poppins;
      color: #000000;
      margin-bottom: 0;
    }
    .total {
      font: normal normal normal 14px/21px Poppins;
      color: #4d4d4d;
    }
    li {
      font-size: 15px;
    }
  }
}
</style>
