<template>
    <div class="app">
        <comp style="position: fixed;"></comp>
    </div>
</template>

<script>
import comp from "../src/preloader.vue"

export default {
    data() {
        return {

        }
    },
    methods: {},
    components: {
        comp
    }
}
</script>
>

<style>
.app {
    margin: 10%;
    padding: 10%
}
</style>