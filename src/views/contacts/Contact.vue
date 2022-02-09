<template>
  <div class="about">
    <h1>This is an contact page list</h1>
    <div v-for="contact in contacts" :key="contact.id">
      <router-link :to="{ name: 'ContactDetails', params: { id: contact.id } }">
        <p>{{ contact.title }}</p>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      contacts: [
        { id: 1, title: "Contact1", gmail: "contact1@gmail", fb: "dsadsa.fb" },
        { id: 2, title: "Contact2", gmail: "contact2@gmail", fb: "sdfdsf.fb" },
        {
          id: 3,
          title: "Contact3",
          gmail: "contact3@gmail",
          fb: "fdsfdsfs.fb",
        },
      ],
    };
  },
  mounted() {
    fetch("https://disease.sh/v3/covid-19/all")
      .then((res) => res.json())
      // .then((data) => this.contact = data)
      .then((data) => console.log(data))
      .catch((err) => console.log(err.message));
  },
};
</script>
