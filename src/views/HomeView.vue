<script setup lang="ts">
  import TheWelcome from '@/components/TheWelcome.vue'
  import CountButton from '@/components/CountButton.vue'
  import CountNumber from '../components/CountNumber.vue'
  import TextBoxVue from '@/components/TextBox.vue';
  import { ref } from 'vue';
  import TextBox from '../components/TextBox.vue';
  const num = ref(0)

  function plus() {
    num.value +=1
  }
  function minus() {
    num.value -=1
  }
  function getText(params:number) {
    num.value += params
  }
</script>

<template>
  <main>
    <CountButton text="足す" @click="plus()"/>
    <CountButton text="引く" @click="minus()"/>
    <CountNumber :number="num"/>
    <TextBox @change="getText"/>
  </main>
</template>
