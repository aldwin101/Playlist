<template>
    <div>
        <h2>{{title}}</h2>
        <p>{{artist}}</p>
        <p>{{genre}}</p>
        <button @click="addToPlaylist">Add to playlist</button>
    </div>
</template>

<script>

    export default {
        name : 'PageBody',
        props: {
            title : String,
            artist : String,
            genre : String
        },

        methods: {
            addToPlaylist(){
                this.$root.$emit('songClick',this.title); 
            }
        },
    }
</script>

<style scoped>

</style>