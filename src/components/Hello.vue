<template>
  <div class="hello">

<section class="hero is-danger is-bold">
  <div class="hero-body">
    <div class="container">
      <h1 class="title">
        Greetings{{ user }}
      </h1>
      <h2 class="subtitle">
        You've ran <b>{{ miles }}</b> miles
      </h2>
    </div>
        <div id="google-signin-btn" style="position: absolute; top: 1%; right: 1% "></div>
  </div>
</section>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data() {
    return {
      user: '',
      miles: '0'
     }
    },
  methods: {
    onSignIn: function (googleUser) {
      var profile = googleUser.getBasicProfile();
      var name = profile.getName();
      name.toString();
      name = ", " + name
      this.$set(this, 'user', name);
  }
 },
 mounted() {
    gapi.signin2.render('google-signin-btn', { // this is the button "id"
      onsuccess: this.onSignIn // note, no "()" here
    })
 }
}


</script>

<style> 


</style>