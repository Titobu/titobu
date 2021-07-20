<template>
<div>
    <div class="main">
        <home-main-component/>
    </div>
</div>
</template>

<script>
import HomeMainComponent from "../home/HomeMainComponent";

export default {
    name: "MainComponent",
    components: {
        HomeMainComponent
    }
}
</script>

<style scoped>
.main {
    width: 100%;
    min-height: calc(100vh - 10vh);
}
</style>
