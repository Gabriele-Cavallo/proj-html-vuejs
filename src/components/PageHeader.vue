<script>
    import { store } from '../store.js'
    export default{
        name: 'PageHeader',
        data(){
            return{
                store,
            }
        }
    }
</script>

<template>
    <h1>ciao sono l'header</h1>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-red;
}
</style>