<template>
  <li>
    <h3>{{ topicName }}</h3>
    <p>{{ description }}</p>
    <button @click="selectTopic(id)">Learn More</button>
  </li>
</template>

<script>
export default {
  inject: ['selectTopic'],
  props: ['id', 'topicName', 'description'],
  emits: ['select-topic'],
};
</script>

<!-- use injector without passing props -->
<!-- provide/inject substitute for input output, so that it lets components communicate -->
<!-- only used for parent & child communication -->
<!-- you should not always used provide/inject to replace custom/props -->