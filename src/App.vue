<template>
    <div id="app">
        <Navigation />
        <Splash />
        <DownloadLinks :version="version" :PC="PC" :mac="mac" v-if="loaded" />
        <Features />
        <ReleaseNotes :notes="notes" :date="date" :version="version" v-if="loaded" />
        <About />
        <Footer />
    </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Splash from './components/Splash.vue'
import DownloadLinks from './components/DownloadLinks.vue'
import Features from './components/Features.vue'
import ReleaseNotes from './components/ReleaseNotes.vue'
import About from './components/About.vue'
import Footer from './components/Footer.vue'

export default {
    name: 'app',
    components: {
        Navigation,
        Splash,
        DownloadLinks,
        Features,
        ReleaseNotes,
        About,
        Footer
    },
    data() {
        return {
            PC: '',
            mac: '',
            version: '',
            date: '',
            notes: [],
            loaded: false
        }
    },
    methods: {
        formatDate(rawDateString) {
            let dateParts = rawDateString.split('-')

            let year = dateParts[0]
            let month = dateParts[1]
            let day = dateParts[2]

            this.date = month + '/' + day + '/' + year
        }
    },
    created() {
        let request = new XMLHttpRequest()
        request.open('GET', 'https://api.github.com/repos/thaddeusm/seatsmart-FHSU/releases/latest')

        request.onreadystatechange = (response) => {
            let formattedResponse = JSON.parse(response.target.response)

            this.version = formattedResponse['tag_name']
            this.formatDate(formattedResponse['created_at'].split('T')[0])

            this.notes = formattedResponse['body'].split('- ')
            this.notes.shift()

            let assets = formattedResponse.assets

            for (let i=0; i<assets.length; i++) {
                let link = assets[i]['browser_download_url']

                if (link.indexOf('.dmg') !== -1 && link.indexOf('.blockmap') == -1) {
                    this.mac = link
                } else if (link.indexOf('.exe') !== -1 && link.indexOf('.blockmap') == -1) {
                    this.PC = link
                }
            }   

            this.loaded = true         
        }

        request.send()
    }
}
</script>

<style>
#app {
    font-family: 'Archivo Narrow', sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    background: var(--black);
    height: 100%;
    width: 100%;
}
</style>
