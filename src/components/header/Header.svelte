<script>
    import Navbar from "./navbar/Navbar.svelte";
    const logo = 'img/logo.png'
</script>

<header>
    <img src={logo} alt='Logo'>
    <Navbar/>
</header>

<style>
    header{
        height: 75px;
        width: 100%;
        padding: 20px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        background-color: var(--blanco);
        box-shadow: rgba(0, 0, 0, 0.19) 0px 10px 20px, rgba(0, 0, 0, 0.23) 0px 6px 6px;
    }
    img{
        width:75px;
        
    }
</style>