<template lang="">
    <div>
        <div v-for="list in this.$store.state.news">{{ list.title }}</div>
    </div>
</template>
<script>
//import { fetchNewsList } from '../api/index.js';

export default {
    created() {
        this.$store.dispatch('FETCH_NEWS');
        // fetchNewsList()
        //     .then(response => this.news = response.data)
        //     // eslint-disable-next-line no-console
        //     .catch(error => console.log(error))
    }
}
</script>
<style lang="">
    
</style>