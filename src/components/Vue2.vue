<template>
  <div>
    <p>{{ message }}</p>
    <button @click="sayHello">Change message</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "No message yet",
    };
  },
  computed: {
    getFullName() {
      return `${this.first_name} ${this.last_name}`;
    },
  },
  methods: {
    sayHello() {
      this.message = "Hello world !";
    },
  },
  mounted() {
    console.log("mounted");
  },
  watch: {
    message() {
      console.log("message has changed");
    },
  },
};
</script>
