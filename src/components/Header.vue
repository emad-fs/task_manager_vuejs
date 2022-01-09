<template>
    <header>
        {{title}}
        <Button title="Add task" color="blue"></Button>
    </header>
  
</template>

<script>
import Button from "./Button.vue";

export default {
  name: "Header",
  components: {
    Button,
  },
  props: {
    title: String,
  },
};
</script>