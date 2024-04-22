<script>
    import { store } from '../store.js'

    export default{
        name: 'PageFooter',

        data(){
            return{
                store,
            }
        }
    }
</script>

<template>
    <h1>ciao sono PageFooter</h1>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-blue;
}
</style>