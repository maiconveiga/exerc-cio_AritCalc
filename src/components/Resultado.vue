<script setup>
    const props = defineProps(['result'])
</script>
<template>
    <div>
        <h3>Resultado: {{ result() }}</h3>
    </div>
</template>
<style scoped>
    div{
        background-color: brown;
        padding: 20px;
        color: white;
        border-radius: 10px;
        margin-top: 10px;
    }
</style>