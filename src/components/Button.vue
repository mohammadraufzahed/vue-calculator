<template>
  <button class="btn ms-1">{{ text }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    text: String,
    buttonType: String,
  },
  methods: {},
};
</script>
