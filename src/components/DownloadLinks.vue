<template>
    <section id="downloadLinks">
        <h3>{{ version }}</h3>
        <a href="#" v-scroll-to="'#releaseNotes'">release notes</a>
        <img src="@/assets/download.svg" alt="download icon">
        <a target="_blank" :href="PC" class="download-link">PC</a>
        <a target="_blank" :href="mac" class="download-link">Mac</a>
    </section>
</template>

<script>
export default {
    name: 'DownloadLinks',
    props: ['version', 'PC', 'mac']
}
</script>

<style scoped>
#downloadLinks {
    padding: 50px;
    margin: 0;
    text-align: center;
    background: var(--yellow);
}

img {
    width: 70px;
    display: block;
    margin: 40px auto;
}

a {
    margin-bottom: 40px;
    color: var(--black);
}

.download-link {
    padding: 7px 15px;
    font-size: 30px;
    color: var(--black);
    text-decoration: none;
    background: var(--light-gray);
    border-radius: 5px;
}

.download-link:nth-child(4) {
    margin-right: 40px!important;
}

.download-link:hover {
    box-shadow: 0 0 2px var(--dark-gray);
}
</style>
