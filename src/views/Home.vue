<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
    <FilesList msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import FilesList from '@/components/FilesList.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
    FilesList,
  },
})
export default class Home extends Vue {}
</script>
