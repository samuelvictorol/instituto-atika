<template>
    <q-page class="bg-primary">
        <div class="w100 row justify-center animate__animated animate__fadeIn animate__slow">
            <img
            class="q-pt-lg"
              alt="Quasar logo"
              src="/favicon.ico"
            >
          </div>
          <p class="q-px-md text-card bg-secondary q-mt-md text-center q-py-md text-bold">Contribuir para o
            desenvolvimento
            socioeducativo da cidade de
            Valparaiso de Goiás-GO,
            utilizando práticas
            educacionais, esportivas,
            culturais e de saúde.</p>
        <div class="w100 row justify-center ">
            <img
            class="q-pt-md"
              alt="Quasar logo"
              src="~assets/img3.png"
            >
        </div>
        <div class="w100 row justify-center ">
            <img
              alt="Quasar logo"
              src="~assets/img4.png"
            >
        </div>
        <div class="text-h4 text-center text-primary q-pt-md">Doação 💸💖</div>
        <div class="w100 q-mt-md row justify-center ">
            <img
              alt="Quasar logo"
              src="~assets/img5.png"
            >
        </div>
        <div class="w100 row">
            <q-btn label="Conheça nossa Loja e ainda ajude o projeto!" color="primary" icon="store" class="w100 q-pa-md" @click="goTo('/loja')"/>
        </div>
        <div class="w100 row justify-center items-center q-mt-md">
          <img src="~assets/insta.svg" style="width:30px" alt="">
        <span class="text-h6 text-white q-pl-md">Acompanhe-nos no Instagram!  </span>
        </div>
        <div class="w100 row justify-center ">
            <img
            class="q-pt-md"
              alt="Quasar logo"
              src="~assets/img2.png"
            >
          </div>
          <div class="w100 bg-primary q-py-md row justify-center ">
            <a target="_blank" href="https://www.instagram.com/institutoatika/">
                <img
                class="rounded-borders"
                  style="width:140px; filter:grayscale(1)"
                  alt="instagram logo"
                  src="~assets/insta.png"
                >
              </a>
          </div>
    </q-page>
</template>

<script setup>
import { useRouter } from 'vue-router'
const router = useRouter()

function goTo(to) {
    router.push(to)
}

</script>

<style scoped>
.text-card {
    font-size: 16px;
    color: #806B64;
    background: #E8D4A2;
}  
</style>