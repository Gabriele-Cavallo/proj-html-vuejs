<script>
    import { store } from './store.js';
    import PageHeader from './components/PageHeader.vue';
    import PageMain from './components/PageMain.vue';
    import PageFooter from './components/PageFooter.vue';

    export default{
        components: {
            PageHeader,
            PageMain,
            PageFooter,
        },
        data (){
            return{
                store,
                headerLinks: ['Home', 'Services', 'About', 'Videos', 'Blog', 'Store']
            }
        },
    }
</script>

<template>
    <PageHeader :headerLinks="headerLinks"></PageHeader>
    <main>
    <PageMain></PageMain>
    </main>
    <PageFooter></PageFooter>
</template>

<style lang="scss">
    @use './style/generic';

</style>