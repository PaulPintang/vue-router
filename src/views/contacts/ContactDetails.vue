<template>
  <div>Contact details</div>
  <p>the contact id is {{ id }}</p>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id,
    };
  },
};
</script>
