<script>
export default {
  name: 'RegionsList',
  props: {
    regions: {
      type: Array,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>
&nbsp;
&nbsp;

<template>
  <section>
    <h2>Regiões e suas Especialidades</h2>
    <p>{{ description }}</p>
    <ul>
      <li v-for="region in regions" :key="region.name">
        <strong>{{ region.name }}:</strong> {{ region.specialty }}
      </li>
    </ul>
  </section>
</template>
&nbsp;
&nbsp;

<style scoped>
section {
  max-width: 900px;
  width: 100%;
  background: #fff;
  border-radius: 15px;
  padding: 25px 30px;
  box-shadow: 0 8px 20px rgba(177, 100, 75, 0.15);
  margin-bottom: 30px;
  transition: box-shadow 0.3s ease;
}
section:hover {
  box-shadow: 0 10px 25px rgba(182, 62, 47, 0.3);
}
h2 {
  font-family: 'Playfair Display', serif;
  color: #b63e2f;
  font-weight: 700;
  border-bottom: 3px solid #b63e2f;
  padding-bottom: 8px;
  margin-bottom: 20px;
  font-size: 2rem;
}
p {
  font-size: 1rem;
  color: #5b4538;
  margin-bottom: 15px;
}
ul {
  list-style-type: none;
  padding-left: 0;
}
li {
  margin-bottom: 10px;
  font-size: 1rem;
  color: #5b4538;
}
strong {
  color: #b63e2f;
  font-weight: 700;
}
</style>
