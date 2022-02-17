<script setup>
import Navbar from './components/Navbar.vue'
import Sidebar from './components/Sidebar.vue'
import EmailList from './components/EmailList.vue'
</script>
<template>
  <Navbar />
  
  <div class="app-body">
    <Sidebar />
    <EmailList />
  </div>
</template>

<style>
@import './assets/base.css';

.app{
  height:100vh;
}

.app-body{
  display: flex;
  height: 100vh;
}

.material-icons{
  
}

</style>
