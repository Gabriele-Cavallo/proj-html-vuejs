<script>
    import FirstMainSection from './FirstMainSection.vue';
    import SecondMainSection from './SecondMainSection.vue';

    export default{
        name: 'PageMain',
        components: {
            FirstMainSection,
            SecondMainSection,
        },
        data(){
            return{

            }
        },
    }
</script>

<template>
    <FirstMainSection></FirstMainSection>
    <SecondMainSection></SecondMainSection>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-yellow;
}
</style>