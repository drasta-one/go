<script>
    import { createEventDispatcher } from 'svelte';

    const dispatch = createEventDispatcher();

    async function handlePasteClick() {
        try {
            const text = await navigator.clipboard.readText();
            dispatch('paste', text);
        } catch (err) {
            console.error('Failed to read clipboard contents: ', err);
        }
    }
</script>

<button class="paste-btn" on:click={handlePasteClick}>📋</button>

<style>
    .paste-btn {
        padding: 10px;
        font-size: 16px;
        border: none;
        border-radius: 4px;
        background-color: #9fb5a5; /* Standard single color */
        color: white;
        cursor: pointer;
        transition: background-color 0.3s ease;
        margin-left: 10px;
    }

    .paste-btn:hover {
        background-color: #acb5ae;
        border-radius: 18px;
    }
</style>
