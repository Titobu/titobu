<template>
<div>
    <div class="main">
        <home-main-component/>
        <projects-main-component/>
    </div>
</div>
</template>

<script>
import HomeMainComponent from "../home/HomeMainComponent";
import ProjectsMainComponent from "../projects/ProjectsMainComponent";

export default {
    name: "MainComponent",
    components: {
        HomeMainComponent,
        ProjectsMainComponent
    }
}
</script>

<style scoped>
.main {
    width: 100%;
    min-height: calc(100vh - 10vh);
}
</style>
