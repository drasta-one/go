<script>
    import Core from './Core.svelte';
    import History from './History.svelte';
</script>

<div class="background">
    <div class="container">
        <div class="panel core-panel">
            <Core />
        </div>
        <div class="panel history-panel">
            <History />
        </div>
    </div>
</div>

<style>
    .background {
        background-color: #ffffff;
        background-image: url('/images/background.svg');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        flex: 1;
        padding: 1em;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .container {
        display: flex;
        flex-direction: column;
        width: 100%;
        max-width: 1200px;
        padding: 1em;
        box-sizing: border-box;
        gap: 10em; /* Add gap between panels */
    }

    .panel {
        flex: 1;
    }

    @media (min-width: 768px) {
        .container {
            flex-direction: row;
        }

        .core-panel {
            order: 2;
        }

        .history-panel {
            order: 1;
        }
    }

    @media (max-width: 767px) {
        .container {
            flex-direction: column;
        }

        .core-panel {
            order: 1;
        }

        .history-panel {
            order: 2;
        }
    }
</style>
