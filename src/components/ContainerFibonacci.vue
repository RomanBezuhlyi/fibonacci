<template>
  <div class="container">
    <ImageFibonacci />
    <TitleFibonacci />
    <FormFibonacci />
  </div>
</template>
<script>
import ImageFibonacci from "@/components/ImageFibonacci.vue";
import TitleFibonacci from "@/components/TitleFibonacci.vue";
import FormFibonacci from "@/components/FormFibonacci.vue";
export default {
  name: "App",
  components: {
    ImageFibonacci,
    TitleFibonacci,
    FormFibonacci,
  },
};
</script>
<style>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-left: auto;
  margin-right: auto;
  background-color: #f5f5f5;
  width: 500px;
  height: 700px;
}
</style>
