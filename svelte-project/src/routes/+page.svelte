<script lang="ts">
    import '../app.css'
    import Cabecalho from '$lib/components/Cabecalho.svelte'
    import MinhaLista from '$lib/components/MinhaLista.svelte';
    import Titulo from '$lib/components/Titulo.svelte';

    import categorias from '$lib/json/categorias.json';
    import Categoria from '$lib/components/Categoria.svelte';

</script>

<svelte:head>
    <title>Cook</title>
</svelte:head>

<div class="container-principal">
    <Cabecalho />
    <div class="estilo-principal">
        <div class="minha-lista-container">
            <MinhaLista />
            <div class="divisoria"></div>
        </div>
        <main>
            <Titulo tag='h1'>ingredientes</Titulo>
            <div class="info">
                <p>Selecione abaixo os ingredientes que você deseja usar na refeição:</p>
                <p>* Atenção: consideramos que você tenha em casa sal, pimenta e água.</p>
            </div>

            <ul class="categorias">
                {#each categorias as categoria (categoria.nome)}
                    <Categoria {categoria}/>
                {/each}
            </ul>

        </main>
    </div>
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

    .minha-lista-container {
        margin-bottom: 2rem;
    }

    .divisoria {
        width: 40vw;
        height: 2px;
        background-color: var(--verde);
        margin: 0 auto;
    }

    .info {
        margin-bottom: 3.375rem;
    }

    .info > p {
        line-height: 2rem;
    }
    
    .categorias {
        margin-bottom: 4.6875rem;

        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 1.5rem;
    }
</style>