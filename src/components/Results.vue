<template>
<p>Reaction Time {{ score }} ms</p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        this.score < 350 ? 
            this.rank = 'You are fast!!'
         :
        this.score < 600 ?  
            this.rank = 'Not bad, but keep trying.'
         : 
            this.rank = 'Take your time grandpa.'
        console.log(this.rank)
    }
    // mounted() {
    //     if (this.score < 350) {
    //         this.rank = 'You are fast!!'
    //     } else if (this.score < 450) {
    //         this.rank = 'Not bad, keep trying.'
    //     }
    //     else {
    //         this.rank = 'Take your time grandpa.'
    //     }console.log(this.rank)
    // }
}

</script>

<style>

</style>