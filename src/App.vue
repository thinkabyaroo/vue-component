<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-lg-6">
        <h1>App Vue</h1>
        <Alert v-for="(message,index) in messages" :key="index" :message="message">
        </Alert>
<!--        <Alert message="Hello" color="alert-success" />-->
<!--        <Alert message="OHiYoo" color="alert-info" />-->
<!--        <Alert />-->


      </div>
    </div>

  </div>
</template>

<script>
import Alert from "@/components/Alert";
export default {
  components: {Alert},
  data() {
    return {
      messages: [
          "hello",
          "OHIYOO",
          "Hi Hi",
          "min ga lar"
      ]
    }
  },
}
</script>

<style lang="scss">
@import "~bootstrap/dist/css/bootstrap.min.css";

</style>