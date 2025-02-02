<script>
    import Page from "../../Page.svelte";
	import Paragraph from "../../Paragraph.svelte";
    import { page } from '$app/stores';
	import { onMount } from "svelte";

    $: article = {};
    $: paragraphs = [];

    const path = $page.params.path;

    async function loadContent() {
        fetch("/posts.json")
            .then(req => req.text())
            .then(text => {
                article = JSON.parse(text).filter(post => post.path === path)[0];
            })

        fetch(`/posts/${path}`)
            .then(req => req.text())
            .then(text => {
                paragraphs = text.split(/\n\n/);
            });
    }

    onMount(() => {
        loadContent();
    });
</script>

<style>
    .title {
        text-align: center;
        font-family: var(--condensed), sans-serif;
        font-size: 3em;
    }

    .metadata {
        text-align: center;
    }
</style>

<Page style="background: linear-gradient(0deg, #fdde599f, #fdde59dd), url(/flag.svg) center; background-size: cover;">
    <a href="/">
        <div class="title">{article.title}</div>
        <div class="metadata">{article.metadata}</div>
    </a>
</Page>
<Page>
    {#each paragraphs as paragraph}
    <Paragraph>
        {paragraph}
    </Paragraph>
    {/each}
</Page>