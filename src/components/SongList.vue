<template>
    <div>
        <p>Songs</p>
        <SongListComp v-for="songs in ListOfSongs" :key="songs" :title='songs.title' :artist='songs.artist' :genre='songs.genre'/>
    </div>
</template>

<script>
import SongListComp from './SongListComp.vue'

    export default {
        name : 'SongList',
        components:  {
            SongListComp
        },
        data() {
            return { 
                ListOfSongs : [
                    {
                    title : 'Versace on the Floor',
                    artist : 'Bruno Mars',
                    genre : 'Pop Music'
                    },
                    {
                    title : 'Impossible',
                    artist : 'James Arthur',
                    genre : 'Pop'
                    },
                    {
                    title : 'Love Is Gone',
                    artist : 'SLANDER ft Dylan Matthew ',
                    genre : 'Dance/Electronic'
                    }
                ]
            }
        }
    }
</script>

<style scoped>

</style>