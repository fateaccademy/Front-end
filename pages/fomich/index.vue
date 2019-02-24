<template>
  <div>
    <ul>
      <li v-for="fruit in fruits" :key="fruit.id">
        <h3>{{fruit.name}}</h3>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "index",
    data() {
      return {
        fruits: [
          {id: 1, name: "banana"},
          {id: 2, name: "ananas"},
          {id: 3, name: "cocos"},
        ]
      };
    }
  }
</script>

<style scoped>

</style>
