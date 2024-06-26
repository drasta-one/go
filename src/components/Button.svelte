<script>
    export let text = "Button";
    export let onClick = () => {};
</script>

<button on:click={onClick}>
    {text}
</button>

<style>
    button {
        background-color: #9fb5a5;
        color: #fff;
        border: none;
        padding: 0.5em 1em;
        border-radius: 4px;
        cursor: pointer;
        transition: background-color 0.3s, border-radius 0.3s;
    }

    button:hover {
        background-color: #acb5ae;
        border-radius: 18px; /* Extra curved corners on hover */
    }
</style>
