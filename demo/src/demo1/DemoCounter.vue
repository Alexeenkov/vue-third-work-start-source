<template>
    <demo-container>
        <div class="counter">
            <CounterButton @action="decrement">-</CounterButton>

            <CounterValue :value="count" />

            <CounterButton @action="increment">+</CounterButton>
        </div>
    </demo-container>
</template>

<script setup>
import { ref } from 'vue';
import CounterButton from "./CounterButton.vue";
import CounterValue from "./CounterValue.vue";

const count = ref(0);

/* Метод уменьшения значения */
const decrement = () => {
    count.value = count.value - 1
}

/* Метод увеличения значения */
const increment = () => {
    count.value = count.value + 1
}
</script>

<style lang="scss" scoped>
.counter {
    display: flex;
    align-items: center;
}
</style>