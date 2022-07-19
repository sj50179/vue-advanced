<template lang="">
    <div>
        <div v-for="item in fetchedAsk">{{ item.title }}</div>
    </div>
</template>
<script>
import { mapState } from 'vuex';

export default {    
    computed: {
        ...mapState({
            fetchedAsk: state => state.ask
        })
        // ask() {
        //     return this.$store.state.ask;  
        // }
    },
    created() {
        this.$store.dispatch('FETCH_ASK');
    }
}

</script>
<style lang="">
    
</style>