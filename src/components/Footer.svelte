<script>
    // Function to handle the "Privacy Policy" click
    function handlePrivacyClick() {
        console.log("Privacy Policy clicked");
        // Add your custom logic here, like navigating to the privacy policy page
    }
</script>

<footer>
    <div class="footer-content">
        <span>&copy; 2024 Drasta One</span>
        <button on:click={handlePrivacyClick}>Privacy Policy</button>
    </div>
</footer>

<style>
    footer {
        background-color: #fff;
        border-top: 2px solid #ddd;
        padding: 1em;
        display: flex;
        justify-content: center;
        box-shadow: 0 -2px 4px rgba(0, 0, 0, 0.1);
        position: fixed;
        width: 100%;
        bottom: 0;
    }

    .footer-content {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        max-width: 1200px;
    }

    button {
        background-color: transparent;
        color: #333;
        border: 1px solid #ccc;
        padding: 0.5em 1em;
        border-radius: 4px;
        cursor: pointer;
        transition: border-color 0.3s, color 0.3s;
    }

    button:hover {
        border-color: #333;
        color: #000;
    }
</style>

