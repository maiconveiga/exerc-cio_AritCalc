<script setup>
    const props = defineProps(['a','b','s'])
</script>
<template>
        <div class="calc">
            <input type="number" @keyup="a" class="form-control">
            <select @change="s" class="form-control">
                <option value="+">+</option>
                <option value="-">-</option>
                <option value="*">x</option>
                <option value="/">/</option>
            </select>
            <input type="number" @keyup="b" class="form-control">
        </div>
    

</template>

<style scoped>
.calc{
    display: inline-flex;
    margin: 0 auto;
    background-color: rgb(99, 91, 168);
    width: 100%;
    padding: 50px;
    border-radius: 10px;
}
.form-control{
    margin-left: 5px;

}
@media (max-width:640px) {
    .calc{
        display: block;
    }
    .form-control{
        margin-bottom: 5px;
    }
}
</style>