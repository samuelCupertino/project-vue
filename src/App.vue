<template>
  <Profile />
</template>

<script>
  import Profile from './components/templates/Profile.vue'

  export default {
    name: 'App',
    components: {
      Profile
    }
  }
</script>

<style>
  :root {
    --primary: #62b983bf;
    --secondary: #50ff96;
    --tertiary: #62b983;
    --bgPrimary: #4f966a;
    --bgSecondary: #2e3e4e;
    --bgTertiary: #3a4f67;
    --textPrimary: #e4ffee;
    --textSecondary: #dbffe9;
    --textTertiary: #f7fffa;
  }

  :root body.dark {
    --primary: #35495e;
    --secondary: #62b983;
    --tertiary: #6c697c;
    --bgPrimary: #141128;
    --bgSecondary: #1d1933;
    --bgTertiary: #272242;
    --textPrimary: #e9e9e9;
    --textSecondary: #c4c3ce;
    --textTertiary: #a09fad;
  }

  body {
    font-family: sans-serif;
  }

  * {
    margin: 0;
    padding: 0;
  }

  *::-webkit-scrollbar {
    width: 0px;
  }
  *:hover::-webkit-scrollbar {
    width: 5px;
  }
  *::-webkit-scrollbar-track {
    box-shadow: inset 0 0 5px rgba(128, 128, 128, 0.5); 
    border-radius: 50rem;
  }
  *::-webkit-scrollbar-thumb {
    background: var(--primary); 
    border-radius: 50rem;
  }
  *::-webkit-scrollbar-thumb:hover {
    background: var(--secondary); 
  }

  ul {
    list-style: none;
  }

  input:focus {
    outline: none;
  }
</style>