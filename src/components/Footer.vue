<template>
    <footer>
        <h6>Released under the MIT License | <img src="@/assets/github.svg" alt="github logo" id="github"><a href="https://github.com/thaddeusm/seatsmart-FHSU" target="_blank">Source Code</a></h6>
        <h6>Copyright © 2019 <a href="mailto:tbmccleary@fhsu.edu">Thaddeus McCleary</a></h6>
        <h6><a href="#" v-scroll-to="'#navigationContainer'"><img src="@/assets/up.svg" alt="up arrow" id="up"></a></h6>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
footer {
    padding: 30px 0 15px 0;
    background: var(--yellow);
}

h6 {
    font-weight: 200;
    margin: 20px auto;
    text-align: center;
}

img {
    vertical-align: middle;
}

#github {
    width: 15px;
    margin-right: 5px;
    margin-bottom: 3px;
}

#up {
    width: 30px;
    margin-top: 15px;
}

a {
    color: var(--black);
}
</style>
