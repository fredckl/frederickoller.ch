<template>
  <section class="font-sans">
    <div class="flex items-center content-center h-screen flex-wrap md:w-1/2 sm:w-full mx-auto border-white">

        <div class="m-auto w-full md:w-1/3 md:ml-auto text-center pr-2">
          <img :src="account.avatar_url" :alt="account.name" class="me">
        </div>
        <div class="m-auto w-full text-center md:w-1/2 md:mr-auto md:text-left items-center bg-grey-darkest-transparent">

          <h1 class="font-sans font-normal">
            {{ account.name }}
          </h1>
          <p>
            développeur web
          </p>
          <p class="border-t-2 pt-2 mt-2">
            <i class="fab fa-html5"></i>
            <i class="fab fa-css3-alt"></i>
            <i class="fab fa-js-square"></i>
            <i class="fab fa-vuejs"></i>
            <i class="fab fa-node"></i>
            <i class="fab fa-sass"></i>
            <i class="fab fa-php"></i>
            <i class="fab fa-github-square"></i>

          </p>
        </div>

    </div>


  </section>
</template>

<script>
export default {
  layout: "dark",
  head: {
    title: 'Frédéric KOLLER',
    meta: [
      { name: 'description', content: 'Développeur web fullstack' },
      { name: 'keywords', content: 'html5, css3, javascript, JS, nodeJS, PHP, CakePHP, Laravel, Django' }
    ]
  },
  components: {},

  async asyncData({ app }) {
    let account = await app.$axios.$get("https://api.github.com/users/fredckl");

    return { account };
  }
};
</script>

<style>
.me {
  border-radius: 50%;
  width: 100px;
}

.bg-grey-darkest-transparent {
  background-color: rgba(61, 72, 82, .5);

}
</style>


