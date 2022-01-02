<script lang="ts">
  // add <Theme /> to id "themes" with props name="dark"
    function addTheme(name: string) {
        const theme = new Theme({
        target: document.getElementById("themes"),
        props: {
            name: "dark",
        }
        });
    }
</script>

<div class="footer" id="footer">
    <div class="toolbar" id="toolbar">
        <span>settings</span>
        <span>import</span>
        <span>create</span>
    </div>
    <div class="info">
        <span class="copyright">
            made by <a href="https://bietlxn.com" target="_blank">bietlxn</a> and <a href="https://github.com/" target="_blank">contributors</a>
        </span>
    </div>
</div>

<style>
    .footer {
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        width: 100%;
    }

    .toolbar {
        width: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        color: rgba(255, 255, 255, 0.795);
        background: rgba(255, 255, 255, 0.027);
        text-align: center;
        border-top: 1px solid rgba(255, 255, 255, 0.116);
    }

    .toolbar span {
        cursor: pointer;
        padding: 10px 20px;
        border-top: 1px solid transparent;
    }

    .toolbar span::selection {
        background: none;
        color: none;
    }

    .toolbar span:hover {
        background: rgba(255, 255, 255, 0.067);
        border-top: 1px solid rgb(255, 255, 255);
        color: white;
    }

    .toolbar span:active {
        background: rgba(255, 255, 255, 0.342);
        border-top: 1px solid rgb(255, 255, 255);
        color: rgba(255, 255, 255, 0.808);
    }

    .info {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 100%;
        color: rgba(255, 255, 255, 0.438);
        padding: 6.7px 0px;
        font-size: 13px;
        letter-spacing: 1px;
        background: rgba(255, 255, 255, 0.027);
        text-align: center;
        border-top: 1px solid rgba(255, 255, 255, 0.116);
    }

    .copyright a {
        text-decoration: none;
        color: rgba(255, 255, 255, 0.692);
    }

    .copyright a:hover {
        color: rgb(255, 255, 255);
        text-decoration: underline;
    }
</style>