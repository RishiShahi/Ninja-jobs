<template>
  <h1>Jobs Detail Page</h1>
  <p>The route id: {{id}}</p>
  <h2>Hello this suresh</h2>
  <h2>Hello this suresh</h2>
  <h2>Hello this suresh</h2>
</template>

<script>
export default {
    data(){
        return {
            id: this.$route.params.id
        }
    }
}
</script>

<style>

</style>