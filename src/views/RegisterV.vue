<template>
  <div class="register">
    <v-container>
      <v-row>
        <v-col cols="12" lg="6" class="colOne">
          <div class="registerOne">
            <v-form v-model="valid" ref="form" class="mx-2" lazy-validation>
              <v-text-field
                v-model="name"
                variant="solo"
                placeholder="Name"
              ></v-text-field>
              <v-text-field
                v-model="phone"
                variant="solo"
                placeholder="Phone Number"
              ></v-text-field>
              <v-text-field
                v-model="password"
                variant="solo"
                placeholder="Password"
              ></v-text-field>
              <v-btn class="bg-gray font-weight-bold"> Sign Up </v-btn>
            </v-form>
            <ul
              class="d-flex justify-center align-center mt-16"
              style="gap: 30px"
            >
              <li v-for="icon in icons" :key="icon.id">
                <a :href="icon.link">
                  <v-icon color="#fff">mdi-{{ icon.icon }}</v-icon>
                </a>
              </li>
            </ul>
          </div>
          <div class="overLay"></div>
        </v-col>
        <v-col cols="12" lg="6">
          <div class="registerTwo">
            <span>Ayman Allam</span>
            <h1 class="my-3">CEMcourses</h1>
            <p>Learn Chemistry Like YOU Have Never Learned It Before</p>
            <div>
              <v-btn class="bg-outline"> Learn More </v-btn>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "RegisterVV",
  data() {
    return {
      name: "",
      phone: "",
      password: "",
      valid: "",
      icons: [
        {
          link: "/",
          icon: "facebook",
        },
        {
          link: "/",
          icon: "whatsapp",
        },
        {
          link: "/",
          icon: "youtube",
        },
        {
          link: "/",
          icon: "instagram",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.register {
  background-image: url("../assets/img//login_page_background.jpg");
  // background: #14365d;

  .v-container {
    height: 100vh;
    .colOne {
      position: relative;
      .registerOne {
        margin-top: 150px;
        z-index: 10;
        position: absolute;
        width: 80%;
      }
      .overLay {
        position: absolute;
        background: #14365d;
        height: 100vh;
        width: 125%;
        left: -150px;
        z-index: 0;
        top: -5px;
      }
    }
    .registerTwo {
      margin-top: 150px;
      span,
      h1,
      p {
        color: #14365d;
        font-weight: bold;
      }
      span {
        font-size: 24px;
      }
      h1 {
        font-size: 48px;
      }
      p {
        font-size: 30px;
      }
    }
  }
}
</style>
