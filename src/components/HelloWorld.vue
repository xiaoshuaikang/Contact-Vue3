<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <div id="layout">
    <div class="header">
      头部
    </div>
    <div class="main">
      <div class="menu">
        左侧
      </div>
      <div class="content">
        <img alt="Vue logo" src="../assets/logo.png" />

        <h1>{{ msg }}</h1>

        <p>
          Recommended IDE setup:
          <a href="https://code.visualstudio.com/" target="_blank">VS Code</a>
          +
          <a href="https://github.com/johnsoncodehk/volar" target="_blank">Volar</a>
        </p>

        <p>See <code>README.md</code> for more information.</p>

        <p>
          <a href="https://vitejs.dev/guide/features.html" target="_blank">
            Vite Docs
          </a>
          |
          <a href="https://v3.vuejs.org/" target="_blank">Vue 3 Docs</a>
        </p>

        <button type="button" @click="count++">count is: {{ count }}</button>
        <p>
          Edit
          <code>components/HelloWorld.vue</code> to test hot module replacement.
        </p>
      </div>
    </div>
  </div>

</template>

<style scoped lang="scss">
#layout {
  width: 100%;
  min-width: 1180px;
  height: 100vh;
  display: flex;
  flex-flow: wrap;
  justify-content: start;
  background: rgb(245,247,249);
  .header {
    height: 80px;
    width: 100%;
    background: #42b983;
    position: fixed;
  }
  .main {
    margin-top: 100px;
    width: 100%;
    height: calc(100% - 100px);
    flex: 1;
    display: flex;
    .menu {
      width: 100px;
      height: 100%;
      background: rgb(251,229,200);
    }
    .content {
      height: 100%;
      min-width: 1080px;
      flex: 1;
      margin-left: 20px;
      background: #FFF;
    }
  }
}

a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
