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
                headerLinks: ['Home', 'Services', 'About', 'Videos', 'Blog', 'Store'],
                footerInfo:
                    {
                        socialLinks: [
                            {
                                social: 'fa-brands fa-facebook-f'
                            },
                            {
                                social: 'fa-brands fa-twitter'
                            },
                            {
                                social: 'fa-brands fa-youtube'
                            },
                            {
                                social: 'fa-brands fa-instagram'
                            },
                            {
                                social: 'fa-brands fa-linkedin-in'
                            },
                        ],
                        posts: [
                            {
                                link: 'The best protein shake'
                            },
                            {
                                link: 'Ultimate cardio workout'
                            },
                            {
                                link: 'New juices available now'
                            },
                            {
                                link: 'Tips to find training partner'
                            },
                            {
                                link: '20 best healthy recipes'
                            },
                        ],
                        contacts: [
                            {
                                address: '4746 Tipple Road Michigan 48449',
                                mobile: '1.800.000.0000',
                                email: 'info@your-company.com',
                            }
                        ],
                    },
                    
                
            }
        },
    }
</script>

<template>
    <PageHeader :headerLinks="headerLinks"></PageHeader>
    <main>
    <PageMain></PageMain>
    </main>
    <PageFooter :footerInfo="footerInfo"></PageFooter>
</template>

<style lang="scss">
    @use './style/generic';

</style>