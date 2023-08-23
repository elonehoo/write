<script setup lang="ts">
import Vditor from 'vditor';
import 'vditor/dist/index.css';

const vditor = ref<Vditor | null>(null);

onMounted(() => {
  vditor.value = new Vditor('vditor', {
    width:'50%',
    typewriterMode:true,
    mode:'ir',
    toolbarConfig:{
      hide: true,
    },
    preview:{
      hljs:{
        defaultLang: 'javascript',
        style: 'github-dark'
      }
    },
    after: () => {
      // vditor.value is a instance of Vditor now and thus can be safely used here
      vditor.value!.setValue("**Hey, welcome to writer.**");
      vditor.value?.focus()
    },
  });
});
</script>

<template>
  <div class="flex justify-center items-center">
    <div id="vditor" />
  </div>

</template>
