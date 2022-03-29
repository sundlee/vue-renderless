<template>
  <div>
    <fetch-data url="https://jsonplaceholder.typicode.com/users/1">
      <template v-slot="{ response, loading }">
        <ul v-if="!loading">
          <li>Name: {{response.name}}</li>
          <li>Mail: {{response.email}}</li>
        </ul>
        <div v-if="loading">
          loading...
        </div>
      </template>
    </fetch-data>
  </div>
</template>

<script>
import FetchData from './components/FetchData.vue'

export default {
  name: 'App',
  components: {
    FetchData,
  },
}
</script>