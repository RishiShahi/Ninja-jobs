<template>
  <div v-for="item in items" :key="item.id" class="job">
      <router-link :to="{name : 'jobsDetail', params: {id: item.id}}">
          <h2>{{item.title}}</h2>
      </router-link>
  </div>
</template>

<script>
export default {
   data() {
       return {
           items: [
               {id: 1, title: 'Web Designer', detail: 'Lorem'},
               {id: 2, title: 'UX Designer', detail: 'Lorem'},
               {id: 3, title: 'Front-end Developer', detail: 'Lorem'}
           ]

       }
   }
}
</script>

<style scoped>
  .job h2 {
     max-width: 400px;
     padding: 10px 20px;
     margin: 10px auto;
     border-radius: 10px;
     color: white;
     background: crimson;
     cursor: pointer;
  }
  .job h2:hover {
     color: crimson;
     background: white;
  }
  .job a{
      text-decoration: none;
  }
</style>