<script lang="ts">
    export let ativa = false;
    export let tamanho: "md" | "lg" = "md";
</script>

<!-- svelte-ignore a11y-<code> -->
<div class="tag {tamanho}"
    class:ativa

>
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

    .lg {
        font-size: 1.125rem;
        padding: 1rem 1.5rem;
    }

</style>


<!-- Setting role attribute allows screen readers to know it can be clicked -->
<!-- <div role="button" tabindex="0" aria-label="Back" onclick="mouseAction(event)" onkeyup="keyAction(event)"> -->