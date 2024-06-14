<template>
  <q-layout view="hHh lpR fFf">

    <q-header  class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title class="q-py-xs rounded-borders">
            <img style="height:40px" class="rounded-borders" src="~/assets/logo.png">
        </q-toolbar-title>

        <q-btn dense flat round icon="menu" @click="rightDrawerOpen = !rightDrawerOpen" />
      </q-toolbar>

      <q-tabs align="center">
        <q-route-tab v-for="item in tabItems" :key="item.label" v-bind="item" />
      </q-tabs>
    </q-header>

    <q-drawer class="bg-primary" show-if-above v-model="rightDrawerOpen" side="right" >

        <q-list class="text-white q-pt-md q-pl-sm">
          <template v-for="(menuItem, index) in tabItems" :key="index">
            <q-item clickable :active="menuItem.label === 'Outbox'" v-ripple>
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
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>

  </q-layout>
</template>

<script setup>
import { ref } from 'vue'

const rightDrawerOpen = ref(false)

const tabItems = ref([
  { label: 'Início', iconName: 'home', to: '/', iconColor:'yellow-2' },
  { label: 'Sobre', iconName: 'info', to: '/sobre', iconColor:'blue-2' },
  { label: 'Loja', iconName: 'store', to: '/loja', iconColor:'green-3' },
  { label: 'Contato', iconName: 'email', to: '/contato', iconColor:'pink-2' },
])

</script>