<script lang="ts">
    import Cabecalho from "$lib/components/Cabecalho.svelte";
    import Rodape from "$lib/components/Rodape.svelte";

</script>

<div class="container-principal">
    <Cabecalho />
    <div class="estilo-principal">
        <slot />
    </div>
    <Rodape />
</div>

<style>
    .container-principal {
        display: flex;
        flex-direction: column;
        min-height: 100vh;
    }

    .estilo-principal {
        text-align: center;
        padding: 0 5vw 3.375rem;
        flex: 1;
    }

</style>


