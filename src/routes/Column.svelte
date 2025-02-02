<script>
    export let title = "";
</script>

<style>
    .column {
        flex: 1;
    }

    .title {
        font-size: 2em;
        margin-top: 24px;
        font-family: var(--condensed), sans-serif;
    }
</style>

<div class="column">
    <div class="title">{title}</div>
    <slot></slot>
</div>