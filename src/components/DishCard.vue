<script>
export default {
  name: 'DishCard',
  props: {
    dish: {
      type: Object,
      required: true
    }
  }
}
</script>


<template>
  <div class="dish-card" :title="dish.name">
    <img :src="dish.image" :alt="dish.name" class="dish-image" />
    <div class="dish-content">
      <h3>{{ dish.name }}</h3>
      <p>{{ dish.description }}</p>
    </div>
  </div>
</template>


<style scoped>
.dish-card {
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 3px 15px rgba(182, 62, 47, 0.15);
  background: #fff8f0;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease;
  cursor: default;
}
.dish-card:hover {
  transform: scale(1.05);
  box-shadow: 0 6px 20px rgba(182, 62, 47, 0.3);
}
.dish-image {
  width: 100%;
  height: 180px;
  object-fit: cover;
  border-bottom: 3px solid #b63e2f;
}
.dish-content {
  padding: 15px 18px;
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}
.dish-content h3 {
  margin-top: 0;
  color: #b63e2f;
  font-family: 'Playfair Display', serif;
  font-size: 1.4rem;
  margin-bottom: 10px;
}
.dish-content p {
  flex-grow: 1;
  font-size: 1rem;
  color: #5b4538;
  margin-bottom: 8px;
}
</style>