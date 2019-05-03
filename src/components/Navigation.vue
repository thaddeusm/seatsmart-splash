<template>
    <header id="navigationContainer">
        <section id="logoArea">
            <img src="@/assets/logo.svg" alt="Seatsmart logo">
        </section>
        <h3>Seatsmart</h3>
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
    grid-template-columns: 50% 50%;
    grid-template-areas: "title logo";
    align-items: center;
}

#logoArea {
    grid-area: logo;
    text-align: right;
}

img {
    height: 50px;
    vertical-align: middle;
    margin-right: 5%;
}

h3 {
    grid-area: title;
    margin-left: 5%;
}
</style>
