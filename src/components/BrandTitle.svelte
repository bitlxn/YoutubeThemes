<script lang="ts">
    export let title = "Title: unavaliable";
</script>

<div class="brandTitle">
    <span class="title">{title}</span>
</div>

<style>
    .brandTitle {
        width: 100%;
        background: rgba(255, 255, 255, 0.027);
        text-align: center;
        padding: 10px 0px;
        border-bottom: 1px solid rgba(255, 255, 255, 0.192);
    }

    .title {
        color: transparent;
        background: rgb(0,176,255);
        background: linear-gradient(18deg, rgb(92, 203, 255) 0%, rgb(255, 84, 244) 100%);
        background-clip: text;
        letter-spacing: 4px;
        font-size: 1.5em;
        font-weight: bold;
    }
</style>