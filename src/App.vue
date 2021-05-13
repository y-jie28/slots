<template>
  <app-form>
    <template v-slot:help>
      <p>{{ help }}</p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="email">
      <input type="text" placeholder="username">
      <input type="password" placeholder="password">
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
    <p>Dummy Text</p>
  </app-form>
 
  <app-form>    
    <template v-slot:help>
      <p>This is some help text. </p>
    </template>
    <template v-slot:fields>
      <input type="text" placeholder="name">
      <input type="text" placeholder="message">
    </template>
    <template v-slot:buttons>
      <button type="submit">Submit</button>
    </template>
    </app-form>

    <select v-model="componentName">
      <option value="Home">Home</option>
      <option value="About">About</option>
    </select>

    <keep-alive> 
      
    </keep-alive>

    <component :is="componentName"></component>
</template>

<script>
import AppForm from "./components/Form";
import About from "./components/About";
import Home from "./components/Home";

export default {
  name: "App",
  components: {
    AppForm, // prefixing the name with the word "App", because there's already an element called "form"
    About,
    Home

  },
  data() {
    return {
      componentName: "Home",
      help: "This is some help text. "
    }
  }
};
</script>
