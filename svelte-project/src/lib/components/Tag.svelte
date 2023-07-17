<script>
    export let ativa = false;
    export let selecionavel = false;
    
    function aoClicar(){
        if(selecionavel) {
            ativa = !ativa;
        }
    }

</script>

<!-- svelte-ignore a11y-<code> -->
<div aria-hidden="true" class="tag ativa" class:ativa on:click={aoClicar} >
    <slot></slot>
</div>

<style>
    .tag {
        height: 48px;
        border-radius: 8px;
        padding: 1rem;
        text-align: center;
        color: var(--cor-texto-principal);
        background-color: var(--cinza);

        display: flex;
        justify-content: center;
        align-items: center;
    }

    .ativa {
        color: var(--branco);
        background-color: var(--laranja);
    }
</style>


<!-- Setting role attribute allows screen readers to know it can be clicked -->
<!-- <div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)"> -->