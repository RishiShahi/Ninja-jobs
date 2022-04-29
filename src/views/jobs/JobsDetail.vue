<template>
  <h1>Jobs Detail Page</h1>
  <p>The route id: {{id}}</p>
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