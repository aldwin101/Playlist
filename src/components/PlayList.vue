<template>
    <div>
        <p>My playlist</p>
        <p>{{songs}}</p>
    </div>
</template>

<script>
    export default {
        name : 'PlayList',
        data() {
            return {
                songs : []
            }
        },
        mounted(){
            this.$root.$on('songClick', this.songChoice);
        },
        methods: {
            songChoice(title){
                this.songs.push(title);
                console.log(this.songs);
            }
        }
    }

</script>

<style scoped>

</style>