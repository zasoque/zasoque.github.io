<script>
    export let article;
</script>

<div class="article-item">
    <a href={`/post/${article.path}`}>
        <div class="title">{article.title}</div>
        <div>{article.metadata}</div>
    </a>
</div>

<style>
    .article-item {
        border-top: 1px solid var(--black);
        padding: 18px;
        flex: 1;
        min-width: 240px;
    }

    .article-item:last-child {
        border-bottom: 1px solid var(--black);
    }

    .title {
        font-size: 1.5em;
        font-weight: bold;
    }

    a {
        text-decoration: none;
    }
</style>