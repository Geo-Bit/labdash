<script setup>
import SiteItem from './Site.vue'
import PlexIcon from './icons/IconPlex.vue'
import json from '../../sites.json'
</script>

<template>
  <SiteItem v-for="block in json.sites">
    <template #icon>
      <img :src="block.icon" alt="SiteIcon" width="30" height="30">
    </template>

    <template #heading>
      <a :href="block.url"> {{ block.title }} </a> 
    </template>
    {{block.description}}
  </SiteItem>

</template>
