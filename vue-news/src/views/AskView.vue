<template lang="">
    <div>
        <div v-for="item in ask">{{ item.title }}</div>
    </div>
</template>
<script>
import { fetchAskList } from "../api/index.js";

export default {
    data() {
        return {
            ask: []
        }
    },
    created() {
        // var vm = this;
        // fetchAskList()
        //     .then(function (response) {
        //         // eslint-disable-next-line no-console
        //         console.log(response);
        //         vm.ask = response.data;
        //     })
        //     .catch(function (error) {
        //         // eslint-disable-next-line no-console
        //         console.log(error);
        //     })
        fetchAskList()
            .then(response => this.ask = response.data)
            // eslint-disable-next-line no-console
            .catch(error => console.log(error))
    }
}

</script>
<style lang="">
    
</style>