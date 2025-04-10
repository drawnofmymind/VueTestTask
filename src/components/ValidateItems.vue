<template>
  <div>
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "ValidateItems",
  data() {
    return {
      value: 1,
    };
  },
  mounted() {
    this.$nextTick(() => this.validate());
  },
  methods: {
    validate() {
      this.$slots.default?.forEach((vnode) => {
        if (vnode.componentOptions?.tag === "validate-items") {
          const childComponent = vnode.componentInstance;
          this.value += 1;
          childComponent.validate();

          console.log('test')
        }
      });
    },
  },
};
</script>
