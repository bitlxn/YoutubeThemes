<script lang="ts">
    import App from '../App.svelte';

    export let name = "Error, no name";
    export let active = false;

    export function selectTheme() {
        const theme = localStorage.getItem("theme");
        if (theme) {
            document.documentElement.setAttribute("dataTheme", theme);
        }
    }
</script>

<div class="themeContainer">
    {#if active == true}
        <button class="theme" id="active">
            <div class="title">
                <span>{name}</span>
                <span class="remove">X</span>
            </div>
        </button>
    {:else}
        <button class="theme" id="deactive" on:click={selectTheme}>
            <div class="title">
                <span>{name}</span>
                <span class="remove">X</span>
            </div>
        </button>
    {/if}
</div>

<style>
    .themeContainer {
        margin: 3px 5px 3px 4px;
    }

    .theme {
        border-radius: 5px;
        width: 100%;
        padding: 11px 5px;
        text-align: left;
        color: rgba(255, 255, 255, 0.589);
        background: rgba(0, 0, 0, 0.253);
        border: 1px solid rgba(0, 0, 0, 0.281);
        margin: 3px 0px;
        cursor: pointer;
        letter-spacing: 2px;
    }

    #active {
        color: rgb(255, 255, 255);
        background: rgba(15, 15, 15, 0.89);
        border: 1px solid rgb(255, 255, 255);
    }

    .theme span {
        margin: 0px 0px 0px 4px;
    }

    .theme .remove {
        text-align: center;
        opacity: 0%;
        float: right;
        width: 25px;
    }

    .theme:hover {
        color: rgb(255, 255, 255);
        background: rgba(0, 0, 0, 0.548);
        border: 1px solid rgba(255, 255, 255, 0.281);
    }

    .theme:hover .remove {
        opacity: 100%;
    }

    .theme:hover .remove:hover {
        color: rgb(255, 133, 133);
        background: rgba(255, 56, 56, 0.178);
        border-radius: 10px;
        font-weight: bolder;
    }

    .theme:hover .remove:active {
        color: rgb(255, 0, 0);
        background: rgba(97, 1, 1, 0.178);
    }

    .theme:active {
        color: rgba(255, 255, 255, 0.884);
        background: rgba(88, 88, 88, 0.548);
        border: 1px solid rgb(255, 255, 255);
    }
</style>