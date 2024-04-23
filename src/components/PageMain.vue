<script>
    import FirstMainSection from './FirstMainSection.vue';
    import SecondMainSection from './SecondMainSection.vue';
    import ThirdMainSection from './ThirdMainSection.vue';
    import FourthMainSection from './FourthMainSection.vue';
    import FifthMainSection from './FifthMainSection.vue';
    import SixthMainSection from './SixthMainSection.vue';
    import SeventhMainSection from './SeventhMainSection.vue';
    import EighthMainSection from './EighthMainSection.vue';

    export default{
        name: 'PageMain',
        components: {
            FirstMainSection,
            SecondMainSection,
            ThirdMainSection,
            FourthMainSection,
            FifthMainSection,
            SixthMainSection,
            SeventhMainSection,
            EighthMainSection,
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
    <FifthMainSection></FifthMainSection>
    <SixthMainSection></SixthMainSection>
    <SeventhMainSection></SeventhMainSection>
    <EighthMainSection></EighthMainSection>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-yellow;
}
</style>