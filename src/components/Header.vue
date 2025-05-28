<script>
export default {
  name: 'Header',
  props: {
    title: {
      type: String,
      required: true
    },
    subtitle: {
      type: String,
      required: true
    }
  }
}
</script>


<template>
  <header>
    <h1>{{ title }}</h1>
    <p>{{ subtitle }}</p>
  </header>
</template>


<style scoped>
header {
  max-width: 900px;
  text-align: center;
  margin-bottom: 40px;
}


h1 {
  font-family: 'Playfair Display', serif;
  font-weight: 700;
  font-size: 3rem;
  color: #b63e2f;
  margin-bottom: 10px;
  text-shadow: 1px 1px 3px rgba(182, 62, 47, 0.7);
}


p {
  font-size: 1.2rem;
  color: #6f5846;
  font-weight: 500;
}


@media (max-width: 480px) {
  h1 {
    font-size: 2.4rem;
  }
}
</style>
