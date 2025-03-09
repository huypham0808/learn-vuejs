<script setup>
    const props = defineProps(['testCountView']);
    const emit = defineEmits(['handle-increase', 'handle-data']);
    const onIncrease = () => {
        emit('handle-increase', 10);
    }

    const getData = () => {
        emit('handle-data',{label: 'Hello', value: 10})
    }
</script>


<template>
    <div class="childComponent">This is child commponent</div>
    <div>Count: {{ props.testCountView }}</div>
    <button @click="onIncrease">Increase</button>
    <button @click="getData">Get data</button>
</template>

<style>
    .childComponent {
        color: green;
    }
</style>