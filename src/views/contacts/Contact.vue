<template>
  <div class="about">
    <h1>This is an contact page list</h1>
    <div v-for="contact in contacts" :key="contact.id">
      <p>{{ contact.gmail }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        { id: 1, gmail: "contact1@gmail", fb: "dsadsa.fb" },
        { id: 2, gmail: "contact2@gmail", fb: "sdfdsf.fb" },
        { id: 3, gmail: "contact3@gmail", fb: "fdsfdsfs.fb" },
      ],
    };
  },
};
</script>
