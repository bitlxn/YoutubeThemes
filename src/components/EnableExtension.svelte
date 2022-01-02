<script lang="ts">
    export let isExtensionEnabled = true;
    let enableText = "enabled";

    function toggleExtension() {
        isExtensionEnabled = !isExtensionEnabled;
        if (isExtensionEnabled) {
            enableText = "enabled";
        } else {
            enableText = "disabled";
        }
    }
</script>

<div class="enableExtension">
    <button class="button" id={enableText} on:click={toggleExtension}>{enableText}</button>
</div>

<style>
    .enableExtension {
        font-family: 'Roboto', sans-serif;
        width: 100%;
        text-align: center;
        border: 0px solid transparent;
    }

    .button {
        color: rgba(255, 255, 255, 0.438);
        width: 100%;
        letter-spacing: 2px;
        padding: 7px 0px;
        border: 0px solid transparent;
        background: rgba(255, 255, 255, 0.027);
        text-align: center;
        font-weight: bold;
        padding: 10px 0px;
        cursor: pointer;
    }

    #enabled {
        color: rgba(98, 255, 84, 0.5);
        border-bottom: 1px solid rgba(98, 255, 84, 0.5);
    }

    #enabled:hover {
        color: rgb(98, 255, 84);
        border-bottom: 1px solid rgb(98, 255, 84);
    }

    #disabled {
        color: rgba(255, 87, 87, 0.699);
        border-bottom: 1px solid rgba(255, 87, 87, 0.699);
    }

    #disabled:hover {
        color: rgb(255, 87, 87);
        border-bottom: 1px solid rgb(255, 87, 87);
    }
</style>