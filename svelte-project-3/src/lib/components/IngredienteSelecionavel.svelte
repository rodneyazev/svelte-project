<script lang="ts">
    import { createEventDispatcher } from "svelte";
    import Tag from "./Tag.svelte";
    export let ingrediente: string;

    const dispatch = createEventDispatcher<{
        adicionarIngrediente: string,
        removerIngrediente: string
    }>();

    let selecionado = false;

    function aoClicar(){
        selecionado = !selecionado;
        if(selecionado){
            // dispatch para adicionar ingrediente
            dispatch('adicionarIngrediente', ingrediente);
        } else {
            dispatch('removerIngrediente', ingrediente);
        }
    }

</script>

<button on:click={aoClicar}>
    <Tag ativa={selecionado}>{ingrediente}</Tag>
</button>

<style>
    button {
        cursor: pointer;
    }
</style>