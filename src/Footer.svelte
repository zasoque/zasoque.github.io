<script>
    import Page from "./Page.svelte";
</script>

<style>
    .container {
        padding: 20px 0;
    }

    .column-container {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
    }

    .column {
        flex: 1;
        margin-right: 12px;
        padding-bottom: 24px;
    }

    .list-title {
        font-family: var(--condensed), sans-serif;
        margin-bottom: 12px;
    }
</style>

<Page container="inverse-color">
    <div class="container">
        <div class="column-container">
            <div class="column">
                <div class="list-title">Ügranemapotaçamis</div>
                <div class="list-item"><a href="http://www.shtelo.org/">J Gwangbuwiki</a></div>
                <div class="list-item"><a href="https://me.shtelo.org">J Scîe</a></div>
                <div class="list-item"><a href="https://docs.google.com/spreadsheets/d/1QSqIbmShJiUiJWNB0x8dQzGbb6W1dqEz_LBlP363e_E/edit">Vapy</a></div>
            </div>
            <div class="column">
                <div class="list-title">Uatevanas</div>
                <div class="list-item"><a href="mailto://junhg0211@gmail.com">Ügranemaletera</a></div>
                <div class="list-item"><a href="https://discord.gg/D3URHFc9uy">J Discord</a></div>
            </div>
            <div class="column">
            </div>
            <div class="column">
            </div>
            <div class="column">
                Krifè da Extelofaxasèzasoquéügranemapotaçamis
            </div>
        </div>
    </div>
</Page>