<template>
  <div id="app">
    <RadioGroup v-model="value" :disabled="disabled">
      <RadioItem value="1" label="Значение 1" />
      <RadioItem value="2" label="Значение 2" />
      <RadioItem value="3" label="Значение 3" />
    </RadioGroup>
    <validate-items>
      <div>
        <validate-items> </validate-items>
      </div>
      <div>
        <validate-items>
          <validate-items> </validate-items>
        </validate-items>
      </div>
      <div>
        <validate-items> </validate-items>
      </div>
    </validate-items>
  </div>
</template>
<script>
import RadioGroup from "@/components/RadioGroup.vue";
import RadioItem from "@/components/RadioItem.vue";
import ValidateItems from "@/components/ValidateItems.vue";
export default {
  components: {
    RadioGroup,
    RadioItem,
    ValidateItems,
  },
  data() {
    return {
      value: "",
      disabled: false,
    };
  },
};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
