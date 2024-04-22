<script>
    import FirstMainSection from './FirstMainSection.vue';
    import SecondMainSection from './SecondMainSection.vue';
    import ThirdMainSection from './ThirdMainSection.vue';
    import FourthMainSection from './FourthMainSection.vue';

    export default{
        name: 'PageMain',
        components: {
            FirstMainSection,
            SecondMainSection,
            ThirdMainSection,
            FourthMainSection,
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
    <ThirdMainSection></ThirdMainSection>
    <FourthMainSection></FourthMainSection>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-yellow;
}
</style>