<template>
  <q-layout view="hHh lpR fFf">

    <q-header  class="bg-primary text-white" height-hint="98"  style="overflow:hidden!important;border-bottom: 2px solid #51a7b173;">
      <img  width="150" class="absolute-left" style="left:8%;" src="~/assets/icon-full.png" alt="">

      <q-toolbar>
        <q-toolbar-title class="q-py-xs rounded-borders">
            <img style="height:40px" class="rounded-borders" src="/favicon.ico">
        </q-toolbar-title>

        <q-btn dense flat round icon="menu" @click="rightDrawerOpen = !rightDrawerOpen" />
      </q-toolbar>

      <q-tabs align="center">
        <q-route-tab v-for="item in tabItems" :key="item.label" v-bind="item" />
      </q-tabs>
    </q-header>

    <q-drawer style="border-left: 4px solid #51a7b173;overflow-x: hidden;" class="bg-primary relative" show-if-above v-model="rightDrawerOpen" side="right" >

        <q-list class="text-white q-pt-md q-pl-sm">
          <template v-for="(menuItem, index) in tabItems" :key="index">
            <q-item @click="goto(menuItem.to)" clickable :active="menuItem.label === 'Outbox'" v-ripple>
              <q-item-section avatar>
                <q-icon :color="menuItem.iconColor" :name="menuItem.iconName" />
              </q-item-section>
              <q-item-section style="letter-spacing: .8px;" class="text-bold">
                {{ menuItem.label }}
              </q-item-section>
            </q-item>
            <q-separator :key="'sep' + index"  v-if="menuItem.separator" />
          </template>

        </q-list>
        <img  width="300" class="absolute-bottom-right" src="~/assets/icon-right.png" alt="">
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const rightDrawerOpen = ref(false)

function goto(to) {
  router.push(to)
}	

const tabItems = ref([
  { label: 'Início', iconName: 'home', to: '/', iconColor:'yellow-2' },
  { label: 'Sobre', iconName: 'info', to: '/sobre', iconColor:'blue-2' },
  { label: 'Loja', iconName: 'store', to: '/loja', iconColor:'green-3' },
  { label: 'Contato', iconName: 'email', to: '/contato', iconColor:'pink-2' },
])

</script>