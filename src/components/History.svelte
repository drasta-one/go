<script>
    import { onMount } from 'svelte';

    let history = [];

    // Function to load history from local storage (using random URLs for testing)
    function loadHistory() {
        // For testing purposes, populate with random URLs
        history = [
            'https://example.com/1',
            'https://example.com/2',
            'https://example.com/3',
            'https://example.com/4',
            'https://example.com/5',
            'https://example.com/6',
            'https://example.com/7',
            'https://example.com/8'
        ];
    }

    // Function to clear history
    function clearHistory() {
        history = [];
    }

    // Load history on component mount
    onMount(() => {
        loadHistory();
    });
</script>

<div class="history-container">
    <div class="history-header">
        <img src="/images/history.svg" alt="History Icon" class="history-icon" />
        <h2>History</h2>
    </div>
    {#if history.length > 0}
        <div class="history-list">
            <ul>
                {#each history as url}
                    <li>
                        <a href={url} target="_blank">{url}</a>
                    </li>
                {/each}
            </ul>
        </div>
        <button class="clear-btn" on:click={clearHistory}>Clear History</button>
    {:else}
        <p>Links you redirect will appear here.</p>
    {/if}
</div>

<style>
    .history-container {
        background: #f9f9f9;
        padding: 2em;
        border-radius: 8px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        max-width: 600px;
        margin: 0 auto;
        text-align: center;
    }

    .history-header {
        display: flex;
        align-items: center;
        justify-content: center;
        margin-bottom: 1em;
    }

    .history-icon {
        width: 48px;
        height: 48px;
        margin-right: 8px;
    }

    h2 {
        font-size: 1.5em;
        color: #333;
    }

    .history-list {
        background: #f0f0f0; /* Darker background for the list */
        padding: 10px;
        border-radius: 8px; /* Curved corners */
        max-height: 120px; /* Limit height to 120px */
        overflow-y: auto; /* Add scroll feature */
        margin-bottom: 1em;
    }

    ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
    }

    li {
        margin-bottom: 0.5em;
    }

    a {
        text-decoration: none;
        color: #007bff;
        word-break: break-word; /* Ensure long URLs wrap properly */
    }

    a:hover {
        text-decoration: underline;
    }

    .clear-btn {
        margin-top: 1em;
        padding: 0.5em 1em;
        font-size: 1em;
        border: none;
        border-radius: 8px; /* Curved corners */
        background-color: #9fb5a5;
        color: white;
        cursor: pointer;
        transition: background-color 0.3s ease;
    }

    .clear-btn:hover {
        background-color: #acb5ae;
        border-radius: 18px;
    }

    p {
        font-size: 1em;
        color: #666;
    }
</style>
