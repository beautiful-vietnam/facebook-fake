<template>
  <div>
    <div>
        <my-Header></my-Header>
        <my-Content/>
    </div>
  </div>
</template>

<script>
import MyHeader from './components/header'
import MyContent from './components/content';

export default {
  
  components: {
    MyHeader,
    MyContent
  }
}
</script>

<style>
body{
  margin: 0px;
}

</style>
