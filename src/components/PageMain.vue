<script>
    import HomeMainSection from './HomeMainSection.vue';
    import ServicesMainSection from './ServicesMainSection.vue';
    import VideosMainSection from './VideosMainSection.vue';
    import AboutMainSection from './AboutMainSection.vue';
    import SubAboutMainSection from './SubAboutMainSection.vue';
    import BlogMainSection from './BlogMainSection.vue';
    import StoreMainSection from './StoreMainSection.vue';
    import SubStoreMainSection from './SubStoreMainSection.vue';
    import BottomMainSection from './BottomMainSection.vue';

    export default{
        name: 'PageMain',
        components: {
            HomeMainSection,
            ServicesMainSection,
            VideosMainSection,
            AboutMainSection,
            SubAboutMainSection,
            BlogMainSection,
            StoreMainSection,
            SubStoreMainSection,
            BottomMainSection,
        },
        data(){
            return{

            }
        },
    }
</script>

<template>
    <HomeMainSection></HomeMainSection>
    <ServicesMainSection></ServicesMainSection>
    <VideosMainSection></VideosMainSection>
    <AboutMainSection></AboutMainSection>
    <SubAboutMainSection></SubAboutMainSection>
    <BlogMainSection></BlogMainSection>
    <StoreMainSection></StoreMainSection>
    <SubStoreMainSection></SubStoreMainSection>
    <BottomMainSection></BottomMainSection>
</template>

<style scoped lang="scss">
    @use '../style/partials/variables' as *;

h1{
    color: $palette-yellow;
}
</style>