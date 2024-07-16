<script lang="ts">
import SelecionarIngredientes from './SelecionarIngredientes.vue'
import SuaLista from './SuaLista.vue'

export default {
  data() {
    return {
      ingredientes: ['Alho', 'Manteiga', 'Orégano', 'Azeite', 'Cebola', 'Manjericão', 'Cenoura', 'Salsinha', 'Cebolinha', 'Limão', 'Vinagre', 'Mostarda', 'Mel', 'Açúcar', 'Farinha', 'Leite', 'Ovo', 'Queijo', 'Presunto', 'Peito de frango', 'Carne moída', 'Peixe', 'Camarão', 'Lentilha', 'Feijão', 'Grão-de-bico', 'Arroz', 'Macarrão', 'Batata', 'Mandioca', 'Abóbora', 'Berinjela', 'Abobrinha', 'Couve', 'Espinafre', 'Alface', 'Rúcula', 'Agrião', 'Repolho', 'Brócolis', 'Couve-flor', 'Beterraba', 'Chuchu', 'Pepino', 'Tomate', 'Pimentão', 'Cebola', 'Gengibre', 'Pimenta', 'Açafrão', 'Canela', 'Cravo', 'Noz-moscada', 'Coentro'].sort()
    }
  }, components: {
    SelecionarIngredientes,
    SuaLista
  }
}
</script>

<template>
  <main class="conteudo-principal">
    <section>
      <SuaLista :ingredientes="ingredientes" />
    </section>

    <SelecionarIngredientes />
  </main>
</template>

<style scoped>
.conteudo-principal {
  padding: 6.5rem 7.5rem;
  border-radius: 3.75rem 3.75rem 0rem 0rem;
  background: var(--creme, #FFFAF3);
  color: var(--cinza, #444);

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5rem;
}

@media only screen and (max-width: 1300px) {
  .conteudo-principal {
    padding: 5rem 3.75rem;
    gap: 3.5rem;
  }
}

@media only screen and (max-width: 767px) {
  .conteudo-principal {
    padding: 4rem 1.5rem;
    gap: 4rem;
  }
}
</style>