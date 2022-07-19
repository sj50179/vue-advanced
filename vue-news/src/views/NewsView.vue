<template lang="">
    <div>
        <div v-for="list in news">{{ list.title }}</div>
    </div>
</template>
<script>
import { fetchNewsList } from '../api/index.js';

export default {
    data() {
        return {
            news: []
        }
    },
    created() {
        // var vm = this;
        // fetchNewsList()
        //     .then(function (response) {
        //         // eslint-disable-next-line no-console
        //         console.log(response);
        //         vm.news = response.data;
        //     })
        //     .catch(function(error) {
        //         // eslint-disable-next-line no-console
        //         console.log(error);
        //     })
        fetchNewsList()
            .then(response => this.news = response.data)
            // eslint-disable-next-line no-console
            .catch(error => console.log(error))
    }
}
</script>
<style lang="">
    
</style>