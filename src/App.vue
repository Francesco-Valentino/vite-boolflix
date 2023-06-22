<script>
import AppBody from './components/AppBody.vue';

export default{

    name: "App",
    components:{ 
      AppBody,
    }
}
</script>

<template>
  <AppBody/>
</template>

<style lang="scss">
@import './styles/general.scss';
@import 'bootstrap/scss/bootstrap';
</style>
