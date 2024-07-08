<template>
  <div v-if="isActive">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Tab',
  props: {
    name: { type: String, required: true },
    label: { type: String, required: true }
  },
  inject: ['addTab'],
  computed: {
    isActive() {
      return this.$parent.activeTab === this.name;
    }
  },
  created() {
    this.addTab({ name: this.name, label: this.label });
  }
};
</script>
