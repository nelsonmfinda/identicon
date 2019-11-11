<template>
  <div class="container">
    <h1>My Identicon Generator</h1>
    <div class="section row">
      <div class="input-field col s5 offset-s3">
        <input v-on:input="onInput" id="username" type="text" class="validate" />
        <label class="active" for="username">Your Name</label>
      </div>

      <div class="col s5 offset-s3">
        <h3 class="identicon">
          See here your
          <b>identicon</b>:
        </h3>
        <div v-html="identicon" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Identicon",
  data: function() {
    return {
      username: ""
    };
  },
  computed: {
    identicon: function() {
      return jdenticon.toSvg(this.username, 200);
    }
  },
  methods: {
    onInput: function(event) {
      this.username = event.target.value;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

input[type="text"]:not(.browser-default).validate + label {
  color: #000000;
}

input.valid[type="text"]:not(.browser-default):focus:not([readonly]) {
  border-bottom: 1px solid #000000;
  box-shadow: 0 1px 0 0 #000000ab;
}

.identicon {
  margin-bottom: 1em;
}
</style>
