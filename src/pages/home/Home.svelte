<script>
    import { blur } from 'svelte/transition';
    import ContainerImages from './components/ContainerImages.svelte';
    import DivFeria from './components/DivFeria.svelte';
    const logo = 'img/logo.png'
</script>

<main>
    <section>
        <img src={logo} alt="">
        <h1 transition:blur="{{amount: 5,opacity:0, duration:300}}">Eureka Arte</h1>
        <h4>Artesanias</h4>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore quisquam, accusantium veniam, quod sunt odit nihil facere hic a reiciendis voluptate facilis. Adipisci necessitatibus officiis nesciunt officia sunt amet quis?</p>
    </section>

    <ContainerImages />

    <DivFeria />
</main>

<style>
    main{
        width: 100%;
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        padding: 20px;
        gap: 20px;
        overflow: hidden;
    }

    section{
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        gap: 10px;
    }

    img{
        width: 50%;
        max-width: 350px;
    }

    h1{
        font-family: var(--primaryFont);
        color: var(--azul);
        font-size: 40px;
    }
    h4{
        font-family: var(--primaryFont);
        color: var(--azul);
        font-size: 16px;
    }
    p{
        font-family: var(--secondaryFont);
        font-weight: 800;
        font-size: 20px;
        text-align: center;
        width:80%;
    }
</style>