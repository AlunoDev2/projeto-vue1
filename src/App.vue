<script>
import Header from './components/Header.vue';
import DishCard from './components/DishCard.vue';
import RegionsList from './components/RegionsList.vue';
import Footer from './components/Footer.vue';


export default {
  name: 'App',
  components: {
    Header,
    DishCard,
    RegionsList,
    Footer
  },
  data() {
    return {
      title: 'Culinária do Brasil',
      subtitle: 'Descubra os sabores incríveis do nosso país!',
      introduction:
        'A culinária brasileira é um reflexo da diversidade cultural e regional do país. Cada estado apresenta pratos típicos que encantam pelos sabores e suas histórias.',
      dishes: [
        {
          id: 1,
          name: 'Feijoada',
          image: 'https://www.minhareceita.com.br/app/uploads/2024/10/feijoada-portal-minha-receita.webp',
          description:
            'Prato tradicional feito com feijão preto, carnes salgadas e linguiça, servido com arroz, couve e laranja.'
        },
        {
          id: 2,
          name: 'Pão de Queijo',
          image: 'https://moinhoglobo.com.br/wp-content/uploads/2016/03/44-p%C3%A3o-de-queijo.jpg',
          description:
            'Deliciosos pãezinhos feitos com polvilho e queijo, típicos de Minas Gerais, crocantes por fora e macios por dentro.'
        },
        {
          id: 3,
          name: 'Moqueca Baiana',
          image: 'https://minhasreceitinhas.com.br/wp-content/uploads/2022/06/moqueca-de-peixe-baiana-1200x800.jpg',
          description:
            'Ensopado de peixe com leite de coco, azeite de dendê, tomates e pimentões, tradicional da Bahia.'
        },
        {
          id: 4,
          name: 'Brigadeiro',
          image: 'https://panelinhagrill.com.br/wp-content/uploads/2025/02/Brigadeiro-Gourmet-perfeito-veja-como-fazer-esse-brigadeiro.webp',
          description:
            'Doce feito com leite condensado, chocolate e manteiga, enrolado em bolinhas e coberto com granulado.'
        }
      ],
      regionsDescription:
        'O Brasil tem regiões com culinárias bastante distintas, influenciadas por variadas culturas e ingredientes locais. Confira algumas especialidades por região:',
      regions: [
        { name: 'Norte', specialty: 'Tacacá, comida rica em tucupi e jambu.' },
        { name: 'Nordeste', specialty: 'Acarajé, moqueca e pratos com dendê.' },
        { name: 'Centro-Oeste', specialty: 'Arroz com pequi e churrasco de panela.' },
        { name: 'Sudeste', specialty: 'Feijoada, pão de queijo e virado à paulista.' },
        { name: 'Sul', specialty: 'Churrasco gaúcho e chimarrão.' }
      ]
    };
  }
};
</script>



<template>
  <div id="app">
    <Header :title="title" :subtitle="subtitle" />


    <section>
      <h2>Introdução</h2>
      <p>{{ introduction }}</p>
    </section>


    <section>
      <h2>Pratos Populares</h2>
      <div class="dish-list">
        <DishCard v-for="dish in dishes" :key="dish.id" :dish="dish" />
      </div>
    </section>


    <RegionsList :regions="regions" :description="regionsDescription" />


    <footer>
    Culinária do Brasil
    </footer>
  </div>
</template>


<style>

</style>
