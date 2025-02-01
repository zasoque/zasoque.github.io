<script>
    import Page from "./Page.svelte";

    export let style;
    export let height = "100vh";
</script>

<style>
    .page {
        display: flex;
    }

    .container {
        margin: auto;
        align-self: center;
        width: 100%;
    }
</style>

<Page {style}>
    <div class="page" style="height: {height};">
        <div class="container">
            <slot></slot>
        </div>
    </div>
</Page>