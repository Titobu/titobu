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

            <div class="socials">
                <ul id="socials" class="socials">
                    <li class="git"><a class="socials" href=""><i class="fab fa-git"></i></a></li>
                    <li class="in"><a class="socials" href=""><i class="fab fa-linkedin-in"></i></a></li>
                    <li class="fb"><a class="socials" href=""><i class="fab fa-facebook-f"></i></a></li>
                </ul>
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

/*SOCIALS*/
div.socials {
    position: absolute;
    bottom: 0;
}

ul.socials {
    padding: 1em;
}

li.git {
    font-size: 2em;
}

li.in {
    font-size: 1.3em;
}

li.fb {
    padding-top: 0.5em;
    font-size: 1.1em;
}

a.socials {
    color: inherit;
}


</style>
