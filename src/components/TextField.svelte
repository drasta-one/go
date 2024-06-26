<script>
    import { createEventDispatcher, onMount } from 'svelte';

    export let value = '';
    const dispatch = createEventDispatcher();

    let inputEl;

    function handleInput(event) {
        value = event.target.value;
        dispatch('input', value);
        adjustHeight(event.target);
    }

    function adjustHeight(element) {
        element.style.height = 'auto';
        element.style.height = `${Math.min(element.scrollHeight, 120)}px`; // Adjust max height to 120px for approx 5-6 lines
    }

    onMount(() => {
        adjustHeight(inputEl);
        window.addEventListener('resize', () => adjustHeight(inputEl));
    });
</script>

<div class="input-container">
    <textarea
            bind:this={inputEl}
            bind:value={value}
            on:input={handleInput}
            placeholder="Paste the link here..."
            rows="1"
    ></textarea>
</div>

<style>
    .input-container {
        position: relative;
        display: flex;
        flex-direction: column;
        align-items: stretch;
        width: 100%;
        max-width: 600px;
        margin: 0 auto;
    }

    textarea {
        width: 100%;
        box-sizing: border-box;
        padding: 10px;
        font-size: 16px;
        border: none; /* Remove border */
        border-radius: 8px; /* Curved corners */
        transition: all 0.3s ease;
        resize: none;
        overflow-y: auto;
        background-color: #f0f0f0; /* Light background color for a modern look */
        color: #333; /* Dark text color for contrast */
        max-height: 120px; /* Limit height to approximately 5-6 lines */
    }
</style>
