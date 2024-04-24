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
                headerLinks: [
                    {
                        link: 'Home',
                        section: 'home',
                        badge: '',
                    },
                    {
                        link: 'Services',
                        section: 'services',
                        badge: '',
                    },
                    {
                        link: 'About',
                        section: 'about',
                        badge: '',
                    },
                    {
                        link: 'Videos',
                        section: 'videos',
                        badge: '',
                    },
                    {
                        link: 'Blog',
                        section: 'blog',
                        badge: '',
                    },
                    {
                        link: 'Store',
                        section: 'store',
                        badge: 'new',
                    },
                ],
                footerInfo:
                    {
                        leftCol: [
                            {
                                logo: '../assets/img/logo-2x.png',
                                paragraph: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Adipisci, provident? Nemo dolore impedit nostrum animi soluta itaque at beatae, sequi molestiae cupiditate eaque fugit, corrupti minus id sint ipsa labore.',
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
                            }
                        ],
                        midCol: [
                            {
                                title: 'RECENT POST',
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
                            }
                        ],
                        rightCol: [
                            {
                                title: 'CONTACT INFORMATION', 
                                contacts: [
                                    {
                                        address: '4746 Tipple Road Michigan 48449',
                                        mobile: '1.800.000.0000',
                                        email: 'info@your-company.com',
                                    }
                                ],
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