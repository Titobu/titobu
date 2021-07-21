<template>
<div>
    <div id="header" class="header">
        <div class="logo">
            <a class="logo" href="">titobu<span>;</span></a>
        </div>

        <div class="menu">
            <ul>
                <li><a href="/">Home<span>;</span></a></li>
                <li><a href="/">Projects<span>;</span></a></li>
                <li><a href="/">CV<span>;</span></a></li>
                <li><a href="/">Contact<span>;</span></a></li>
            </ul>
        </div>

        <div class="options">
            <ul>
                <li @click="selectTheme()" v-if="activeTheme === 'light'"><i class="fas fa-moon fa-moon-color"></i></li>
                <li @click="selectTheme()" v-if="activeTheme === 'dark'"><i class="fas fa-sun fa-sun-color"></i></li>
            </ul>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: "HeaderComponent",
    homeRoute: "",
    data: () => {
        return {
            themes: ["light", "dark"],
            activeTheme: "light"
        }
    },
    methods: {
        selectTheme() {
            if (this.activeTheme === this.themes[0])
            {
                this.activeTheme = this.themes[1];

                this.addClassToElementById("app", "to-light-theme-bg", "to-dark-theme-bg");
                this.addClassToElementById("header", "to-light-theme-text", "to-dark-theme-text");
                this.addClassToElementById("socials", "to-light-theme-text", "to-dark-theme-text");
            }else {
                this.activeTheme = this.themes[0];

                this.addClassToElementById("app", "to-dark-theme-bg", "to-light-theme-bg");
                this.addClassToElementById("header", "to-dark-theme-text", "to-light-theme-text");
                this.addClassToElementById("socials", "to-dark-theme-text", "to-light-theme-text");
            }
        },
        setTheme() {
            if (this.activeTheme === this.themes[0])
            {
                this.addClassToElementById("app", "to-dark-theme-bg", "to-light-theme-bg");
                this.addClassToElementById("header", "to-dark-theme-text", "to-light-theme-text");
                this.addClassToElementById("socials", "to-dark-theme-text", "to-light-theme-text");
            }else {
                this.addClassToElementById("app", "to-light-theme-bg", "to-dark-theme-bg");
                this.addClassToElementById("header", "to-light-theme-text", "to-dark-theme-text");
                this.addClassToElementById("socials", "to-light-theme-text", "to-dark-theme-text");
            }
        },
        addClassToElementById(elementId, classNameToRemove, classNameToAdd) {
            let element = document.getElementById(elementId);
            element.classList.remove(classNameToRemove);
            element.classList.add(classNameToAdd);
        }

    },
    mounted() {
        this.setTheme();
    }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Saira+Stencil+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@600&family=Saira+Stencil+One&display=swap');


.header {
    width: 100%;
    height: 10vh;
    min-height: 2rem;
    display: flex;
    justify-content: space-around;
    align-items: flex-end;
}

/*LOGO*/
a.logo{
    font-family: 'Saira Stencil One', cursive;
    box-sizing: border-box;
    font-size: 2rem;
    line-height: 1.2;
    /*color: #131313;*/
    color: inherit;
}

a:hover {
    text-decoration: none;
}

span{
    color: darkred;
}

/*MENU*/
ul {
    margin: 0;
    padding: 0;
}
li{
    display: inline-block;
    list-style: none;
    cursor: pointer;
}

li a{
    font-family: 'Poppins', sans-serif;
    padding: 0 10px;
    color: inherit;
}

/*OPTIONS*/

.fa-sun-color{
    color: yellow;
}

.fa-moon-color{
    color: #1f1f1f;
}

</style>
