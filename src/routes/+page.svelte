<script>
    import OnePage from "./OnePage.svelte";
    import Page from "./Page.svelte";
    import Content from "./Content.svelte";
    import Paragraph from "./Paragraph.svelte";
    import ArticleItem from "./ArticleItem.svelte";

    import "bootstrap-icons/font/bootstrap-icons.css";
	import { onMount } from "svelte";

    $: articles = [];

    onMount(async () => {
        const req = await fetch("/posts.json");
        const text = await req.text();
        const posts = JSON.parse(text);
        posts.sort((a, b) => b.id - a.id);
        articles = posts.splice(0, 5);
    });
</script>

<style>
    .title {
        font-family: var(--condensed), sans-serif;
        font-size: 3em;
    }

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

    .page-header {
        font-family: var(--condensed), sans-serif;
        font-size: 2em;
        margin-bottom: 12px;
    }
</style>

<OnePage style="background: linear-gradient(0deg, #f7f7f9dd, #f7f7f99f), url(/flag.svg) center; background-size: cover;">
    <Paragraph><span class="title">Feloxipùno da Zasoque!</span></Paragraph>
    <Paragraph>Aniska, Sat!</Paragraph>
    <Paragraph>
        <div class="chevron">
            <i class="bi bi-chevron-down"></i>
        </div>
    </Paragraph>
</OnePage>
<Page>
    <div class="page-header">Novépotaçamisis</div>
    {#each articles as article}
        <ArticleItem {article}/>
    {/each}
</Page>