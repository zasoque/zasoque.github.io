<script>
    import OnePage from "./OnePage.svelte";
    import Page from "./Page.svelte";
    import Content from "./Content.svelte";
    import Column from "./Column.svelte";
    import Paragraph from "./Paragraph.svelte";
    import Metadata from "./Metadata.svelte";

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
</style>

<OnePage style="background: linear-gradient(0deg, #f7f7f9dd, #f7f7f99f), url(/flag.svg) center; background-size: cover;">
    <Column title="Feloxipùno da Zasoque!">
        <Paragraph>Aniska, Sat!</Paragraph>
        <Paragraph>
            <div class="chevron">
                <i class="bi bi-chevron-down"></i>
            </div>
        </Paragraph>
    </Column>
</OnePage>
<Page>
    <Content>
        <Column title="Zasoqûm quavùll">
            <Paragraph>
                Zasoquas J Zasoque da krifìç é Krinatio.
            </Paragraph>
            <Paragraph>
                «Krinatio»-s Insürtiksùmim izàhull, Sioquedas laro Stara'l gorùll krifùquê Énatiol draviàsum.  Zasoquas ä Spiquèho; Zasospiqua'l gorùll krifùquê. Spiquas ä Has da poirnùqûm Íckosum raspùquefe Krifùquie izìa, Zasoque d'iks Ésiros'um ä Natio lar'ä Megias'as iksàhe. Ad J Zasoque da tagèull tou Spiqual oh öxùie Krifìl gorùllas Natio d'unas, J Chrisanctheséspiqual krifìçéie Liszt; J Paul Louis samie tiägè lo Maquê-Sat, ad Zasoque l'Hirénatè iksùm umie Sat roy vexàse.
            </Paragraph>
            <Metadata>Zasoque Scîe, 2025-Ärgê 1-Télital, 22:49</Metadata>
        </Column>
        <Column title="Diséügranemapotaçamis">
            <Paragraph>
                Disas Ügranemapotaçamisèzasoque. Màtaupùm quavùll um Zasoque um Disépotaçamis. Zasoquémegias lo lofanàro, Zasospiqual nòlofanùtum um difaxas.
            </Paragraph>
            <Paragraph>
                Diséügranemapotaçamisas 2025-Ärgê 1-Télital'um krifùquê. J Gaurosseaux d'ironarisùll quavùll um Linnam, J Zasoque da tagè tou hòinosùdum Jélinnamè quavùm um Zasoque. Ä Zozaqûis J Extelom quav Élinnam suan hòvagìçeular.
            </Paragraph>
            <Paragraph>
                Zasoquélinnam lo inosèular, maxé Zasokrifi'l krifùll, ö niram Vizaxàsutil gorùll zequàd.  Üpa!
            </Paragraph>
            <Metadata>Zasoque Scîe, 2025-Ärgê 1-Télital, 22:27</Metadata>
        </Column>
    </Content>
</Page>