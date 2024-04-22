<script>
    import FirstMainSection from './FirstMainSection.vue';
    export default{
        name: 'PageMain',
        components: {
            FirstMainSection,
        },
        data(){
            return{

            }
        },
    }
</script>

<template>
    <FirstMainSection></FirstMainSection>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-yellow;
}
</style>