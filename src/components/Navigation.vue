<template>
    <header id="navigationContainer">
        <section id="logoArea">
            <img src="@/assets/logo.svg" alt="Seatsmart logo">
        </section>
        <h3>Seatsmart <span id="subtitle">| class participation manager</span></h3>
        <section id="linkArea">
            <a href="https://mailfhsu-my.sharepoint.com/:v:/g/personal/tbmccleary_fhsu_edu/ERWcdtM1yBJPhffl5rvttiwBP8JNyhQA9_RoBg-kEkw4Pw?e=iyrKnZ" target="_blank">Walkthrough</a>
            <a href="https://github.com/thaddeusm/seatsmart-FHSU/wiki/Development-Roadmap-(Academic-Year-2019-2020)" target="_blank">Roadmap</a>
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
    grid-template-columns: 30px auto auto;
    grid-template-areas: "logo title links";
    align-items: center;
}

#logoArea {
    grid-area: logo;
    text-align: left;
}

img {
    width: 30px;
    vertical-align: middle;
    margin-right: 10px;
}

h3 {
    grid-area: title;
    margin-left: 3%;
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
    margin: 0 10px;
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
