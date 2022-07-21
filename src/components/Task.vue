<template lang="">
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>{{task.text}}
            <fa icon="xmark"/>
        </h3>
        <p>{{task.day}}</p>
    </div>
</template>
<script>


export default {
  name: "Task",
  props: {
    task: Object,
  },
};
</script>
<style scoped>
    .task {
        background: #F4F4F4;
        margin: 5px;
        padding: 10px 20px;
        cursor: pointer;
    }

    .task.reminder{
        border-left: 5px solid green;
    }

    .task h3{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
</style>