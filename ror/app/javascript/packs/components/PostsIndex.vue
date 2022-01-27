<template>
  <div>
    <ul>
      <li v-for="post in posts" :key="post.id">
        Nota bene: {{ post.name }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'PostsIndex',
  props: {
    posts: {
      type: Array,
      default: () => [
        {name: 'p1'}, 
        {name: 'p2'}, 
        {name: 'p3'}
      ]
    }
  },
  data: function () {
    return {
      message: "Stupid message"
    }
  }
}
</script>

<style scoped>
p {
  font-size: 2em;
  text-align: center;
}
</style>
