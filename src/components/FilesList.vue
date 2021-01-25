<template>
  <div class="files-list">
    <ul>
      <li v-for="(file, index) in list" :key="index">
        <a :href="file.path">
          {{ file.name }}
        </a>
      </li>
    </ul>

    <button @click="onClick">Click!</button> {{ count }}
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component
export default class FilesList extends Vue {
  // Initial data can be declared as instance properties
  message = 'Hello!';

  list = [
    {
      name: 'pdf',
      path: '../assets/CROQUIS 3 D761.pdf',
    },
    {
      name: 'fullstack',
      path: '../assets/fullstack.jpg',
    },
  ];

  count = 0;

  onClick(): void {
    this.count += 1;
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}

a {
  color: #42b983;
}
</style>
