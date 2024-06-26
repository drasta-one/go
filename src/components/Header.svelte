<script>
    import Button from './Button.svelte';
    // Function to handle the "Custom" button click
    function handleCustomClick() {
        console.log("Custom button clicked");
        // Add your custom logic here
    }
</script>

<header>
    <div class="header-content">
        <img src="/images/go_transparent.png" alt="Logo" class="logo" />
        <Button text="Custom" on:click={handleCustomClick} />
    </div>
</header>

<style>
    header {
        background-color: #fff;
        border-bottom: 2px solid #ddd;
        padding: 1em;
        display: flex;
        justify-content: center;
        box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    }

    .header-content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        max-width: 1200px;
    }

    .logo {
        height: 60px; /* Adjust the height as needed */
    }
    .logo:hover {
        filter: drop-shadow(0 0 2em #ff3e00aa);
    }
</style>
