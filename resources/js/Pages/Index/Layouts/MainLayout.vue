<script setup>
import {Link} from "@inertiajs/vue3";
import {ref} from "vue";

const timer = ref(0)
const intervalId = setInterval(() => {
    timer.value++
}, 1000)

const stopInterval = function () {
    clearInterval(intervalId);
}

</script>

<template>
    <Link href="/">Main Page</Link>&nbsp;
    <Link href="/hello">Show Page</Link>
    <div>The page with time {{ timer }}</div>
    <button v-on:click="stopInterval">Stop Interval</button>
    <slot>Default</slot>
</template>

<style scoped>

</style>
