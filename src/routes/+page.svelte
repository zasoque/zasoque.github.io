<script>
    import OnePage from "../OnePage.svelte";
    import Page from "../Page.svelte";
    import Footer from "../Footer.svelte";

    import "bootstrap-icons/font/bootstrap-icons.css";
</script>

<style>
    .chevron {
        margin-top: 24px;
        font-size: 1.5em;
        animation: bounce 2s infinite;
    }

    @keyframes bounce {
        0%, 20%, 50%, 80%, 100% {
            transform: translateY(0);
        }
        40% {
            transform: translateY(-10px);
        }
        60% {
            transform: translateY(-5px);
        }
    }

    .title {
        font-size: 2em;
        margin-top: 24px;
        font-family: var(--condensed), sans-serif;
    }

    .content {
        display: flex;
        gap: 20px;
    }

    .column {
        flex: 1;
        max-height: 320px;
    }

    .column-2 {
        flex: 2;
        max-height: 320px;
    }

    .column-3 {
        flex: 3;
        max-height: 320px;
    }

    .paragraph {
        margin-top: 0.5em;
    }

    .metadata {
        color: #2c2c2c9f;
        font-size: 0.8em;
        margin-top: 0.5em;
    }

    .metadata::before {
        content: "- ";
    }
</style>

<OnePage style="background: linear-gradient(0deg, #f7f7f9dd, #f7f7f99f), url(/flag.svg) center; background-size: cover;">
    <div class="title">Feloxipùno da Zasoque!</div>
    <div class="content">Aniska, Sat!</div>
    <div class="content chevron" bind:this={ chevron }><i class="bi bi-chevron-down"></i></div>
</OnePage>
<Page>
    <div class="content">
        <div class="column">
            <div class="title">Zasoqûm quavùll</div>
            <div class="paragraph">
                Zasoquas J Zasoque da krifìç é Krinatio.
            </div>
            <div class="paragraph">
                «Krinatio»-s Insürtiksùmim izàhull, Sioquedas laro Stara'l gorùll krifùquê Énatiol draviàsum.  Zasoquas ä Spiquèho; Zasospiqua'l gorùll krifùquê. Spiquas ä Has da poirnùqûm Íckosum raspùquefe Krifùquie izìa, Zasoque d'iks Ésiros'um ä Natio lar'ä Megias'as iksàhe. Ad J Zasoque da tagèull tou Spiqual oh öxùie Krifìl gorùllas Natio d'unas, J Chrisanctheséspiqual krifìçéie Liszt; J Paul Louis samie tiägè lo Maquê-Sat, ad Zasoque l'Hirénatè iksùm umie Sat roy vexàse.
            </div>
            <div class="metadata">Zasoque Scîe, 2025-Ärgê 1-Télital, 22:49</div>
        </div>
        <div class="column">
            <div class="title">Diséügranemapotaçamis</div>
            <div class="paragraph">
                Disas Ügranemapotaçamisèzasoque. Màtaupùm quavùll um Zasoque um Disépotaçamis. Zasoquémegias lo lofanàro, Zasospiqual nòlofanùtum um difaxas.
            </div>
            <div class="paragraph">
                Diséügranemapotaçamisas 2025-Ärgê 1-Télital'um krifùquê. J Gaurosseaux d'ironarisùll quavùll um Linnam, J Zasoque da tagè tou hòinosùdum Jélinnamè quavùm um Zasoque. Ä Zozaqûis J Extelom quav Élinnam suan hòvagìçeular.
            </div>
            <div class="paragraph">
                Zasoquélinnam lo inosèular, maxé Zasokrifi'l krifùll, ö niram Vizaxàsutil gorùll zequàd.  Üpa!
            </div>
            <div class="metadata">Zasoque Scîe, 2025-Ärgê 1-Télital, 22:27</div>
        </div>
    </div>
</Page>
<Footer />