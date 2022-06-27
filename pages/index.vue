<template>
    <div class="container">
        <h1>
            Index page
            name: {{ store.name }}
        </h1>
        <button @click="show">Show user name</button>
    </div>
</template>

<script setup>
import { useStore } from '@/store/user';

const store = useStore()
const name = ref(store.name)
function show() {
    console.log(store.name)
}
</script>