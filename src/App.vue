<script setup lang="ts">
import DaysInMonth from './components/DaysInMonth.vue'
import TheWelcome from './components/TheWelcome.vue'



</script>

<template>
    <header>
        <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

        <div class="wrapper">
            <DaysInMonth year="2023" month="5"></DaysInMonth>
        </div>
    </header>

    <main>
        <TheWelcome />
    </main>
</template>

<style scoped>
header {
    line-height: 1.5;
}

.logo {
    display: block;
    margin: 0 auto 2rem;
}


</style>
