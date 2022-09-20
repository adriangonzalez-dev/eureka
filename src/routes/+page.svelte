<script>
    import {Router, Route} from 'svelte-routing'
    import Footer from '../components/footer/Footer.svelte';
    import Header from '../components/header/Header.svelte';
    import Contacto from '../pages/contacto/Contacto.svelte';
    import Home from '../pages/home/Home.svelte';
    import Productos from '../pages/productos/Productos.svelte';
</script>

<Router >
    <Header/>
    <Route path='/' >
        <Home/>
    </Route>

    <Route path='/productos'>
        <Productos/>
    </Route>

    <Route path='/contacto'>
        <Contacto/>
    </Route>
    <Footer/>
</Router>
