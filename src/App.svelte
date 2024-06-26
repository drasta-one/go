<script>
    import Header from './components/Header.svelte';
    import Footer from './components/Footer.svelte';
    import ContentMain from './components/ContentMain.svelte';
</script>

<main>
    <Header appName="Go" />
    <ContentMain />
    <Footer />
</main>

<style>
    main {
        padding: 0;
        font-family: Arial, sans-serif;
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }
</style>
