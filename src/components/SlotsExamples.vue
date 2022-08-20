<template>
  <div class="hello">
    <main>
      <slot name="title"></slot>
    </main>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "slotsExamples",
  data() {
    return {};
  },
};
</script>
