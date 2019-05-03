<template>
    <section id="releaseNotes">
        <h2>Lastest Release:</h2>
        <h3>{{ version }} | {{ date }}</h3>
        <ul>
            <li v-for="note in notes">{{ note }}</li>
        </ul>
    </section>
</template>

<script>
export default {
    name: 'ReleaseNotes',
    props: ['notes', 'date', 'version']
}
</script>

<style scoped>
#releaseNotes {
    background: var(--light-gray);
    text-align: center;
    padding: 100px 0;
}

h3 {
    margin: 20px 0 50px 0;
}

ul {
    list-style: none;
    text-align: center;
    max-width: 800px;
    margin: 0 auto;
}

li {
    margin: 20px 0;
    padding: 0 25px;
    max-width: 800px;
    text-align: left;
    line-height: 1.8;
}
</style>
