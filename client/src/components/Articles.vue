<template>
  <div class="col-md-9">
    <div class="article" v-for="article in childarticles">
      <div class="panel panel-default">
        <div class="panel-heading"><router-link :to="{ path: '/blog/' + article._id, params: {} }"><h2>{{ article.title }}</h2></router-link></div>
        <div class="panel-body">
          <img :src="article.image" alt="image" class="img-responsive" />
        </div>
        <div class="panel-body">
          <p>{{ article.article }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ['childarticles'],
  name: 'Articles',
  data () {
    return {
      msg: 'Hello Articles'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
