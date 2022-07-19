<template lang="">
    <div>
        <div v-for="job in jobs">{{ job.title }}</div>
    </div>
</template>
<script>
import { fetchJobsList } from "../api/index.js";

export default {
    data() {
        return {
            jobs: []
        }
    },
    created() {
        // var vm = this;
        // fetchJobsList()
        //     .then(function (response) {
        //         // eslint-disable-next-line no-console
        //         console.log(response);
        //         vm.jobs = response.data;
        //     })
        //     .catch(function (error) {
        //         // eslint-disable-next-line no-console
        //         console.log(error);
        //     })
        fetchJobsList()
            .then(response => this.jobs = response.data)
            // eslint-disable-next-line no-console
            .catch(error => console.log(error))
    }
}

</script>
<style lang="">
    
</style>