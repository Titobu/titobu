<template>
    <div>
        <div class="hero">
            <img src="https://nafie.webrouk.com/assets/images/hero-img.png" alt="hero">

            <div class="content">
                <div class="title">
                    <h2>We Design & Build <br> Creative Products</h2>
                </div>

                <div class="button-get-in-touch">
                    <a class="button" href="">GET IN TOUCH</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "HomeMainComponent"
}
</script>

<style scoped>
.hero{
    height: calc(100vh - 10vh);
    width: 100%;
    text-align: center;
    background-image: url("/images/hero-back.png");
    background-repeat: no-repeat, repeat;
    background-position: center top; /* Center the image */
    position: relative;
}

img{
    max-height: 100%;
}

.content {
    position: absolute;
    bottom: 10%;
    width: 100%;
    color: white;

}

h2 {
    font-size: 3rem;
}

.title {
    padding-bottom: 10%;
}

a.button {
    padding: 0.5rem 1rem;
    border: 1px solid white;
    border-radius: 5px;
    color: white;
    text-decoration: none;
    font-size: 1.2rem;
}
</style>
