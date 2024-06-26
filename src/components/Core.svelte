<script>
    import TextField from './TextField.svelte';
    let longLink = '';
    let shortLink = '';

    function handleShortenClick() {
        if (longLink.trim() === '') {
            alert('Please enter a link.');
            return;
        }

        // Placeholder for URL shortening logic
        shortLink = `https://short.url/${btoa(longLink).slice(0, 8)}`;
    }

    function copyToClipboard() {
        navigator.clipboard.writeText(shortLink).then(() => {
            alert('Shortened URL copied to clipboard!');
        });
    }
</script>

<div class="plank">
    <div class="input-group">
        <TextField bind:value={longLink} />
        <button class="shorten-btn" on:click={handleShortenClick}>Generate Short URL</button>
    </div>
    {#if shortLink}
        <div class="short-link">
            <span>{shortLink}</span>
            <button on:click={copyToClipboard}>Copy</button>
        </div>
    {/if}
</div>

<style>
    .plank {
        background: #f9f9f9;
        padding: 2em;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        text-align: center;
        max-width: 600px;
        margin: 0 auto;
    }

    .input-group {
        margin-bottom: 1em;
        display: flex;
        flex-direction: column;
        align-items: stretch;
        width: 100%;
    }

    .shorten-btn {
        margin-top: 10px;
        padding: 10px;
        font-size: 16px;
        border: none;
        border-radius: 8px; /* Curved corners */
        background-color: #9fb5a5;
        color: white;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    .shorten-btn:hover {
        background-color: #acb5ae;
        border-radius: 18px;
    }

    .short-link {
        margin-top: 1em;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .short-link span {
        padding: 0.75em;
        background: #fff;
        border: 1px solid #ccc;
        border-radius: 4px;
        margin-right: 0.5em;
        font-size: 1em;
        cursor: text;
    }
</style>

