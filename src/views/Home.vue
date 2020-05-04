<template>
  <div id="dash" ref="dash1" class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import DockManager from "../../lib/js/DockManager";

// ../../lib/js/DockManager
export default {
  name: "Home",
  components: {
    HelloWorld
  },
  methods: {},
  created() {
    console.log("hello");

    this.$nextTick(() => {
      const element = this.$refs;
      console.log(document);

      console.log(this.$refs.dash1);

      const dockManager = new DockManager(element);
      console.log(`created - ${dockManager}`);

      dockManager.initialize();
    });

    console.log("inside");
  }
};
</script>
