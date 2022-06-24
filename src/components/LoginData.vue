<template>
  <div>
    <h1>Data</h1>
    <ul>
      <li>{{ username }}</li>
      <li>{{ name }}</li>
      <li>{{ surname }}</li>
      <li>{{ email }}</li>
    </ul>
    <h2>JWT</h2>
    <p>{{ jwt }}</p>
    <h3>Decoded JWT</h3>
    <div v-for="(value, name) in decodedJwt" v-bind:key="(value)">
      {{ name }}: {{ value }}
    </div>
    <h3>Resource access</h3>
    <p v-if="resource_access==null">test</p>
    <p>{{ resource_access }}</p>
  </div>
</template>

<script>
export default {
  name: "LoginData",
  props: {
    name: String,
    surname: String,
    username: String,
    email: String,
    jwt: String,
    decodedJwt: Object,
    resource_access: Object,
  }
}
</script>

<style scoped>

</style>