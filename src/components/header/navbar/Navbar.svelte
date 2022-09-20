<script>
    import { Link } from "svelte-routing";
    import { quintOut } from 'svelte/easing';
    import { slide } from 'svelte/transition';
    let active = false;

    const activeMenu = () =>{
        active ? active = false : active = true
    }

</script>

    <button on:click={()=>activeMenu()}>
        <i class="fa-solid fa-bars"></i>
    </button>
    {#if active}
        <nav transition:slide="{{delay: 250, duration: 300, easing: quintOut }}">
            <ul>
                <li on:click={()=>activeMenu()}><Link to='/'>Home</Link></li>
                <li on:click={()=>activeMenu()}><Link to='/productos'>Productos</Link></li>
                <li on:click={()=>activeMenu()}><Link to='/contacto'>Contacto</Link></li>
            </ul>
            
        </nav>
    {/if}

<style>
    nav{
        position: absolute;
        top:75px;
        left:0;
        width:100vw;
        height: 75vh;
        background-color:var(--blanco);
        font-family: var(--primaryFont);
        font-weight: 600;
        z-index: 9999;
    }

    ul{
        display: flex;
        flex-direction: column;
        justify-content: space-evenly;
        align-items: center;
        width:100%;
        height: 100%;
    }

    li{
        list-style: none;
        color: var(--azul);
        font-size: 50px;
    }

    button{
        width: 40px;
        height: 40px;
        font-size: 35px;
        color:var(--azul);
        background: none;
        border:none;
        outline: none;
    }

</style>