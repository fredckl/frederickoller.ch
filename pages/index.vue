<template>
  <section class="font-sans">
    <div class="flex h-screen flex-wrap w-full border-white">

        <div class="mt-auto md:my-auto text-center w-full md:w-1/4 px-4 pb-3 md:text-left items-center">
          <div class="md:pl-12 md:ml-2">
            <img src="/frederickoller.png" alt="Frédéric KOLLER - développeur web" class="me mb-3 shadow">
          </div>

          <h1 class="font-normal">
            Frédéric KOLLER
          </h1>
          <p>
            développeur web
          </p>
          <p class="border-t-2 pt-2 mt-2 clearfix">
            <i class="fab fa-html5" title="Expert HTML5"></i>
            <i class="fab fa-css3-alt" title="Expert CSS et CSS 3"></i>
            <i class="fab fa-js-square" title="Expert Javascript"></i>
            <i class="fab fa-vuejs" title="Junior VueJS"></i>
            <i class="fab fa-node" title="Junior NodeJS"></i>
            <i class="fab fa-sass" title="Maitrise Sass"></i>
            <i class="fab fa-php" title="Expert PHP"></i>
            &nbsp;
            &nbsp;
            &nbsp;
            <span class="contact float-right">

              <a href="//github.com/fredckl" class="text-grey-dark" title="Frédéric KOLLER - Mon Github">
                <i class="fab fa-github"></i>
              </a>

              <a href="//www.linkedin.com/in/frederic-koller" class="text-grey-dark" title="Frédéric KOLLER - Me suivre sur LinkedIn">
                <i class="fab fa-linkedin-in"></i>
              </a>
              <a href="#" class="text-grey-dark" @click.prevent="openMail" title="Frédéric KOLLER - Me contacter par e-mail">
                <i class="far fa-envelope"></i>
              </a>
            </span>

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
      { name: 'keywords', content: 'html5, css3, javascript, JS, nodeJS, PHP, CakePHP, Laravel, Django' }
    ]
  },
  components: {},

  data () {
    return {
      email: 'moc.liamg__f.rellok'
    }
  },

  methods: {
    getEmail () {
      return this
        .email
        .split('')
        .reverse()
        .join('')
        .replace('__', '@')
    },
    openMail () {
      window.location.href = "mailto:" + this.getEmail()
    }
  },

  async asyncData({ app }) {
    // let account = await app.$axios.$get("https://api.github.com/users/fredckl");

    // return { account };
  }
};
</script>

<style>
.me {
  border-radius: 50%;
  border: 1px #a2a2a2 solid;
  width: 100px;
}
.contact > a {
  margin-left: .2rem;
  transition: all .5s;
}
.contact > a:hover {
  color: #F8FAFC;
}
.cursor-pointer {
  cursor: pointer;
}
</style>


