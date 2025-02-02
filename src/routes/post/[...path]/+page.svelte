<script>
    import Page from "../../Page.svelte";
    import Column from "../../Column.svelte";
	import Paragraph from "../../Paragraph.svelte";
	import Metadata from "../../Metadata.svelte";
    import { page } from '$app/stores';
	import { onMount } from "svelte";

    let article;
    $: title = "";
    $: paragraphs = [];
    $: metadata = "";

    const path = $page.params.path;

    async function loadContent() {
        const req = await fetch(`/posts/${path}`);
        const text = (await req.text());
        title = text.match(/^# (.*)\n/)[1];
        const content = text.substring(3 + title.length);
        paragraphs = content.split(/\n\n/);
        metadata = paragraphs.splice(paragraphs.length-1)[0];
    }

    onMount(() => {
        loadContent();
    });
</script>

<Page>
    <Column {title}>
        {#each paragraphs as paragraph}
        <Paragraph>
            {paragraph}
        </Paragraph>
        {/each}
        <Metadata>{metadata}</Metadata>
    </Column>
</Page>