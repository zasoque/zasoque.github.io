<script>
    export let container = "";
    export let style;
</script>

<style>
    .container {
        padding: 24px 0;
    }

    .page {
        max-width: 800px;
        margin: auto;
        padding: 0 24px;
    }

    .inverse-color {
        color: var(--white);
        background-color: var(--black);
    }
</style>

<div class="container {container}" {style}>
    <div class="page">
        <slot></slot>
    </div>
</div>