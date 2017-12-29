<template>
<div class="hello">
  <h1>{{ msg }}</h1>

     <button type="button"
             class="btn btn-primary" autocomplate="off"
             data-loading-text="jquery with bootstrap"
             @click="clickBtn">
       Click
     </button>

  </div>
</template>


<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      msg: 'Vue.js'
    }
  },
  methods: {
    clickBtn(event) {
      this.msg = '2014.04.16';
    }
  },
  mounted() {
    this.$nextTick( () => {
      jQuery('hello').hide();
      $('.hello').fadeIn('slow');
    })
  }
}
</script>

<style scoped>

.hello {
  margin-top: 50px;
}

.btn-primary {
  margin : 20px 0;
}

h1,
h2 {
  font-weight: normal;
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
</style>
