<script>
    import Tag from "./Tag.svelte";

    let ingredientes = ['Alho', 'Manteiga', 'Ovos']

</script>

<section class="minha-lista">
    <h2>Sua lista:</h2>
    <ul class="meus-ingredientes">
        {#each ingredientes as ingrediente (ingrediente)}
            <Tag ativa={true}>{ingrediente}</Tag>
        {/each}
    </ul>
</section>

<style>
    .minha-lista {
        padding-bottom: 1.625rem;
    }

    .minha-lista > h2 {
        font-size: 1.5rem;
        color: var(--laranja);
        margin-bottom: 1.5rem;
        line-height: 2rem;
        font-weight: 700;
    }

    .meus-ingredientes {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 0.75rem 1.875rem;
    }
</style>
