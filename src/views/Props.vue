<template>
  <div>
    <Child :greeting="greeting" :icecream="icecream" />
  </div>
</template>

<script>
import Child from "../components/Child";

export default {
  data() {
    return {
      greeting: "SRY MR. WHALEN",
      icecream: ["I", "WILL", "DO", "BETTER ASAP"],
    };
  },
  components: {
    Child,
  },
};
</script>

<style></style>
