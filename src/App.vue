<template>
  <app-form>
    <div class="help">
      <p>This is some help text. </p>
    </div>
    <div class="fields">
      <input type="text" placeholder="email">
      <input type="text" placeholder="username">
      <input type="password" placeholder="password">
    </div>
    <div class="buttons">
      <button type="submit">Submit</button>
    </div>
  </app-form>
</template>

<script>
import AppForm from "./components/Form"

export default {
  name: "App",
  components: {
    AppForm, // prefixing the name with the word "App", because there's already an element called "form"
  }
};
</script>
