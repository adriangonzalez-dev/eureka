<script>
    const wsp = 'img/wsp.png'

    export let name;
    export let image;
    export let price;
    export let category;

    let active = false;

    const liked = () =>{
        active ? active = false : active=true;
        localStorage.setItem('liked',active)
    }

</script>


<div class="wrapper">
	<div class="image">
        <img src={image} alt="">
        <span on:click={()=>liked()}>
            <i class={`fa-solid fa-heart ${active ? 'liked' : ''}`}></i>
        </span>
    </div>
    <div class="info">
            <h4>{name}</h4>
            <p>${price}</p>
            {#if category === 'espejo'}
                <p>Envio gratis <i class="fa-solid fa-truck-fast"></i></p>
            {/if}
            <div class="shop">
                <p>Categoría: {category}</p>
                <a href="/"><img src={wsp} alt=""></a>
            </div>
    </div>
</div>

<style>
    div.wrapper{
        width: 100%;
        max-width: 400px;
        display: flex;
        gap: 10px;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 0px 8px;
    }

    div.image{
        width: 45%;
        position: relative;
        display: flex;
        align-items: center;
    }

    div.image img{
        width: 100%;
        border-radius: 5px;
    }

    div.image span{
        position:absolute;
        top: 5px;
        right: 5px;
        width: 25px;
        height: 25px;
        border-radius: 50%;
        background-color: var(--blanco);
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
    }

    div.image span i{
        -webkit-text-stroke: 1px black;
        color: white;
        font-size: 12px;
    }

    div.image span i.liked{
        -webkit-text-stroke: 1px var(--azul);
        color: var(--azul);
    }

    div.info{
        padding: 0px 10px 0px 10px;
        display: flex;
        align-items: flex-start;
        justify-content: center;
        font-family: var(--secondaryFont);
        font-size: 18px;
        width: 100%;
        flex-direction: column;
        
    }

    div.shop{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
    }

    div.shop a{
        width: 20px;
        height: 20px;
    }

    div.shop a img{
        width:100%;
    }

    div.info p i{
        color:var(--azul)
    }

</style>