<template>
    <div>
        <div><header-component/></div>
        <div><main-component/></div>
        <div><footer-component/></div>
    </div>
</template>

<script>
    import HeaderComponent from "./parts/HeaderComponent";
    import MainComponent from "./parts/MainComponent";
    import FooterComponent from "./parts/FooterComponent";

    export default {
        name: 'App',
        mounted() {
            console.log('Component mounted.')
        },
        components: {
            HeaderComponent,
            MainComponent,
            FooterComponent
        }
    }
</script>
