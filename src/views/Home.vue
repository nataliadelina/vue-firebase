<template>
  <div class="container text-center">
    <div class="row justify-content-center">
      <div class="text-secondary text-center">
        welcome back <span class="font-weight-bold">{{ user }}</span>
      </div>
      <div class="col-10 col-md-10 col-lg-8 col-xl-7">
        <h4 class="display-4 text-primary mt-3 mb-2">Meeting Log</h4>
        <p class="lead">
          This simple app creates meetings, allows people to check in, and picks
          random users to award giveaways. It's a good example of a Single Page
          Application which includes connection to a database and routing. It's
          a practical way to learn
          <a href="https://vuejs.org/">Vue.js</a>
          with
          <a href="https://firebase.google.com">Firebase</a>.
          <font-awesome-icon
            class="text-danger"
            icon="star"
          ></font-awesome-icon>
        </p>

        <router-link class="btn btn-outline-primary mr-2" to="/register"
          >Register</router-link
        >
        <router-link class="btn btn-outline-primary mr-2" to="/login"
          >Log In</router-link
        >
        <router-link class="btn btn-primary" to="/meetings"
          >Meetings</router-link
        >
      </div>
    </div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import db from "../db";

export default {
  name: "home",
  components: {
    FontAwesomeIcon,
  },
  data() {
    return {
      user: null,
    };
  },
  mounted() {
    db.collection("users")
      .doc("AmkGqYvyrb2mv3TqbErs")
      .get()
      .then((snapshot) => {
        this.user = snapshot.data().name;
      });
  },
};
</script>
