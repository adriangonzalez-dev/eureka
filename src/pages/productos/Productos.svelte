<script>
    import {productos} from '../../store/images';
    import CardProduct from './components/CardProduct.svelte';
    import Search from './components/Search.svelte';
    let search = ''
    const handleSubmit = () =>{
        console.log(search)
    }
</script>

<main>
    <Search {search} {handleSubmit}/>
    <article class="productContainer">
        {#each productos as producto}
            <CardProduct 
            name={producto.name}
            image={producto.image}
            price={producto.price}
            category={producto.category}/>
        {/each}
    </article>
</main>

<style>
    main{
        width: 100%;
        display: flex;
        flex-direction: column;
        
        align-items: center;
        justify-content: center;
        gap: 15px;
    }
    article.productContainer{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        width: 100%;
        align-items: center;
        justify-content: center;
        gap: 10px;
    }
</style>