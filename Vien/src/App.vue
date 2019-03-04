<template>
  <div>
    <div>
        <myHeader></myHeader>
        <myContent/>
    </div>
  </div>
</template>

<script>
import myHeader from './components/header'
import myContent from './components/content';

export default {
  
  components: {
    myHeader,
    myContent
  }
}
</script>

<style>
body{
  margin: 0px;
}

</style>
