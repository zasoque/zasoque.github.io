<style>
    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 24px 0;
        position: fixed;
        width: 100vw;

        background-color: var(--grey);
        color: var(--white);
    }

    .content {
        display: flex;
        align-items: center;
        width: 1080px;
        margin: auto;
        padding-left: 24px;
    }

    .logo {
        display: flex;
        align-items: center;
        margin-right: 36px;
        text-shadow: var(--black) 0px 5px 10px;
    }

    .logo-img {
        width: 2em;
        border-radius: 50%;
        box-shadow: var(--black) 0px 5px 10px;
    }

    .logo-title {
        font-size: 1.5em;
        margin-left: 10px;
        font-family: var(--condensed), sans-serif;
    }

    .navigation-items {
        display: flex;
        gap: 20px;
    }
</style>

<div class="container" bind:this={container}>
    <div class="content">
        <div class="logo">
            <img src="./favicon.png" alt="Logo" class="logo-img" />
            <span class="logo-title">Eraxeniluinsèzasoque</span>
        </div>
        <div class="navigation-items">
            <a href="#top">Taicìe</a>
        </div>
    </div>
</div>