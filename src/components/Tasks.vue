<template>
    <div :key="task.id" v-for="task in tasks">
        <task-vue @delete-task="onDelete(task.id)" :task="task"/>
    </div>
</template>

<script>
import taskVue from "./task.vue";

export default {
  name: "Tasks",
  components:{
      taskVue,
  },
  props: {
    tasks: Array,
  },
  methods:{
      onDelete(id){
          this.$emit('delete-task',id)
      }
  },
  emits: ['delete-task']
};
</script>