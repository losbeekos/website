<template>
  {{ age }}
</template>

<script setup lang="ts">
import { differenceInYears } from 'date-fns'

const age = differenceInYears(new Date(), new Date(1985, 6, 25));
</script>
