<script>
    import Icons from "./icons/Icons.svelte";


</script>

<footer>
    <Icons/>
    <p>Desarrollado por <a href="/">adriangonzalez.dev90</a></p>
</footer>

<style>
    footer{
        height: fit-content;
        width: 100%;
        background-color:var(--blanco);
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        font-family: var(--secondaryFont);
        font-weight: 900;
        padding: 10px;
        gap: 5px;
        box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;
    }
</style>