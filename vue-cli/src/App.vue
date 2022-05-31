<template>
  <div>
    {{ msg }}
    <app-header v-bind:propsdata="msg" v-on:renew="renewStr"></app-header>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      msg: "hihi",
    };
  },
  components: {
    "app-header": AppHeader,
  },
  methods: {
    renewStr: function () {
      this.msg = "hi!!";
    },
  },
};
</script>

<style></style>
