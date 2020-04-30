<template>
  <ol>
    <li v-for="person in list" :key="person">
      {{ person.firstname }} {{ person.lastname }}
    </li>
  </ol>
</template>

<script>
export default {
  props: ['list'],
};
</script>
