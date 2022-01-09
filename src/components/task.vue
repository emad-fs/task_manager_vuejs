<template>
    <div :class="[task.reminder ? 'reminder' : '','task']">
        <h3>{{task.text}}
            <i @click="onDelete" class="fas fa-times"></i>
        </h3>
        <p>{{task.reminder}}</p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props:{
        task: Object,
    },
    methods:{
        onDelete(id){
            this.$emit('delete-task',id)
        }
    }
}
</script>

<style scoped>
.fas {
  color: rgb(0, 0, 0);
}
.task {
  background: #f4f4f4;
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>