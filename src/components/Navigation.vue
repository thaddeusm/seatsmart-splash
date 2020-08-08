<template>
    <header id="navigationContainer">
        <section id="logoArea">
            <img src="@/assets/logo.svg" alt="Seatsmart logo">
        </section>
        <h3>Seatsmart <span id="subtitle">| class participation manager</span></h3>
        <section id="linkArea">
            
        </section>
    </header>
</template>

<script>
export default {
    name: 'Navigation'
}
</script>

<style scoped>
#navigationContainer {
    height: 70px;
    background: var(--light-gray);
    display: grid;
    grid-template-rows: auto;
    grid-template-columns: 50px auto auto;
    grid-template-areas: "logo title links";
    align-items: center;
}

#logoArea {
    grid-area: logo;
    text-align: center;
}

img {
    width: 40px;
    vertical-align: middle;
}

h3 {
    grid-area: title;
    margin-left: 1%;
    text-align: left;
}

#subtitle {
    color: var(--gray);
}

#linkArea {
    grid-area: links;
    text-align: right;
}

a {
    color: var(--black);
    text-decoration: none;
    margin-right: 20px;
}

a:hover {
    text-decoration: underline;
}


@media screen and (max-width: 800px) {
    #subtitle {
        display: none;
    }
}
</style>
