<template>
  <div class="social">
    <section class="container">
      <div class="row">
        <div
          class="col-md-6 offset-md-3"
          v-for="(sns, index) in links"
          :key="index"
        >
          <div>
            <img class="sns mx-auto" v-bind:src="sns.icon" />
            <h2>
              <a v-bind:href="sns.link">{{ sns.name }}</a>
            </h2>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "social",
  data() {
    return {
      links: [
        {
          name: "twitter",
          icon: require("@/assets/twitter.png"),
          link: "https://twitter.com/ntaso_2051"
        },
        {
          name: "github",
          icon: require("@/assets/github-icon.png"),
          link: "https://github.com/ntaso2051"
        }
      ]
    };
  }
};
</script>

<style>
.sns {
  width: 120px;
}
</style>
