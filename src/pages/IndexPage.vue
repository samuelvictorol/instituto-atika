<template>
  <q-page class="bg-primary animate__animated animate__fadeIn animate__slow">
    <div class="w100 row justify-center ">
      <img
      class="q-pt-lg"
        alt="Quasar logo"
        src="/favicon.ico"
      >
    </div>
    <p class="q-px-md text-card bg-secondary text-center q-py-lg q-mt-md text-bold">INSTITUTO ÁTIKA é uma associação civil sem fins lucrativos, dedicada à causas sociais</p>
    <div class="w100 row justify-center ">
      <img
      id="img-1"

      class="q-pt-md q-px-xl"
        alt="Quasar logo"
        src="~assets/image1.png"
      >
    </div>
    <p class="q-px-md text-card bg-secondary text-center q-mt-lg q-py-md text-bold">
      Se você é apaixonado por futevôlei e busca um local que una esporte, conforto e gastronomia de qualidade, a Arena Átika é o seu destino ideal. Estamos orgulhosos de apresentar o mais novo conceito em arenas de futevôlei, onde cada detalhe foi pensado para proporcionar uma experiência única e inesquecível para nossos visitantes.
    </p>
    <div class="w100 row justify-center ">
      <img
      class="q-pt-md"
        alt="Quasar logo"
        src="~assets/insta2.png"
      >
    </div>
    <p class="q-px-md bg-secondary text-card text-center q-mt-md q-py-md text-bold">
      Esporte: na Arena Átika, o futevôlei é mais do que um esporte – é uma paixão. Nossas instalações modernas e bem equipadas oferecem tudo o que você precisa para jogar em alto nível, seja você um iniciante ou um atleta experiente. Com quadras de areia finas e bem cuidadas, iluminação de ponta para jogos noturnos e um ambiente vibrante, garantimos a melhor experiência possível para praticantes de todas as idades e habilidades.
    </p>
    <div class="w100 row justify-center ">
      <img
      class="q-pt-md"
        alt="Quasar logo"
        src="~assets/insta3.png"
      >
    </div>
    <p class="bg-secondary q-px-md text-card text-center q-mt-lg q-py-md text-bold">
      Gastronomia: e para tornar sua visita ainda mais especial, a Arena Átika oferece uma experiência gastronômica diferenciada. Nosso restaurante, liderado por chefs renomados, apresenta um cardápio diversificado que agrada a todos os paladares. Desde refeições leves e saudáveis até pratos mais elaborados, nossa gastronomia é pensada para complementar a energia e o prazer do futevôlei. Aproveite para degustar nossas especialidades enquanto assiste aos jogos ou relaxa após suas partidas.
    </p>
    <div class="w100 row justify-center ">
      <img
      class="q-pt-md"
        alt="Quasar logo"
        src="~assets/insta4.png"
      >
    </div>
    <p class="bg-secondary q-px-md text-card text-center q-mt-md q-py-md text-bold">
      Um Lugar Para Todos: a Arena Átika é um espaço inclusivo e acolhedor, perfeito para famílias, amigos e atletas. Promovemos um ambiente amigável e seguro, onde todos podem desfrutar da prática esportiva e do convívio social. Além disso, realizamos eventos e torneios regulares, oferecendo a oportunidade de competir, socializar e, claro, se divertir.
    </p>
    <div class="w100 row justify-center ">
      <img
      class="q-pt-md"
        alt="Quasar logo"
        src="~assets/insta5.png"
      >
    </div>
    <p class="q-px-md text-card text-center q-mt-md q-py-md text-bold">
      <q-btn  label="Sobre o Projeto" icon="help" icon-right="skip_next" color="accent" @click="goto('/sobre')"/>
    </p>
    <div class="w100 row justify-center ">
      <img
        alt="Quasar logo"
        src="~assets/img1.png"
      >
    </div>
    <div class="text-h6 q-pt-md text-center text-white">🌍 Onde nos Encontrar ?</div>
    <iframe class="q-mt-md" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3833.4856211157776!2d-47.971570531451185!3d-16.092160610856578!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x935985fb8ad5237f%3A0xae60a41becde95ac!2sArena%20%C3%81tika%20Futev%C3%B4lei!5e0!3m2!1spt-BR!2sbr!4v1718389921647!5m2!1spt-BR!2sbr" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
    <div class="column justify-center items-center bg-primary q-py-lg">
      <a class="q-pt-md" target="_blank" href="https://www.instagram.com/institutoatika/">
        <img
        class="rounded-borders"
          style="width:140px; filter:grayscale(1)"
          alt="instagram logo"
          src="~assets/insta.png"
        >
      </a>
      <a style="filter: grayscale(1) invert(1); border:2px solid black; border-radius:4px" target="_blank" class="q-pa-sm q-mt-sm row text-bold justify-center items-center" href="https://www.instagram.com/arenaatika/">
        <img
        style="width:20px;"
          src="~assets/insta.svg"
        >
        <span class=" text-black q-pl-sm">Arena Átika</span>
      </a>
      <a id="dev-by" class="w100 row no-wrap justify-center items-center q-py-lg" target="_blank" href="https://samuelvictorol.github.io/portfolio/">
        Desenvolvido por Samuel Victor
        <q-icon class="q-pl-md" name="code" color="accent" size="md"/>
      </a>
    </div>
    <LoadingComponent v-if="loading" />
  </q-page>
</template>

<script setup>
import LoadingComponent from 'src/components/LoadingComponent.vue';
import { onBeforeMount, ref } from 'vue';
import { useRouter } from 'vue-router'
const router = useRouter()
const loading = ref(true)
function goto (to) {
  router.push(to)
}

onBeforeMount(() => {
  setTimeout(() => {
    loading.value = false
  }, 4000) 
})
</script>
<style scoped>
.text-card {
  font-size: 16px;
  color: #806B64;
  background: #201E1F;
}
#img-1 {
  padding: 0px;
  width: 60vw;
  height: auto
}

@media (max-width: 600px) {
  #img-1 {
    padding: 0px;
    width: 90vw;
    height: 500px;
  }
}

</style>