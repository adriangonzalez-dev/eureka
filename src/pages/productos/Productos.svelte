<script>
    import { productos } from "../../store/images";
    import CardProduct from "./components/CardProduct.svelte";
    import Search from "./components/Search.svelte";
    import Swal from 'sweetalert2'

    let searchProduct;
    let products = [];
    const handleSubmit = () => {

        let productsFilter = productos.filter((producto) =>
        producto.name.includes(searchProduct.trim())
        );

        if(!searchProduct || productsFilter.length == 0){
            Swal.fire({
            title: 'Error!',
            text: 'No hay resultados para la búsqueda',
            icon: 'error',
            confirmButtonText: 'Cerrar'
            })
        }else{
            products = [...productsFilter];
            console.log(searchProduct)
        }
    };

    $: newProducts = products.length == 0 ? productos : products;
</script>

<main>
    <Search bind:search={searchProduct} {handleSubmit} />

    <article class="productContainer">
        {#each newProducts as producto}
            <CardProduct
                name={producto.name}
                image={producto.image}
                price={producto.price}
                category={producto.category}
            />
        {/each}
    </article>
</main>

<style>
    main {
        width: 100%;
        min-height: 79vh;
        display: flex;
        flex-direction: column;

        align-items: center;
        justify-content: flex-start;
        gap: 15px;
    }
    article.productContainer {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        width: 100%;
        align-items: center;
        justify-content: center;
        gap: 10px;
    }
</style>
