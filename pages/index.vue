<template>
  <div class="container">
    <div>
      <Component1 v-if="valid" />
      <Component2 v-else />
      <button @click="valid = true">
        Switch components
      </button>
    </div>
  </div>
</template>

<script>
const Component1 = () => import("~/components/Component1.vue");
const Component2 = () => import("~/components/Component2.vue");
export default {
  components: {
    Component1,
    Component2,
  },
  data: () => ({
    valid: false,
  }),
};
</script>
