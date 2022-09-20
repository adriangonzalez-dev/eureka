<script>
    export let name;
    export let image;
    export let price;
    
    const wsp = 'img/wsp.png'

</script>

<!--<div>
    <h4>{name}</h4>
    <img src={image} alt={name}>
    <div class='hoverCard'>
        ${price}
        <a href="/">
            <p>Reservar</p>
            <img src={wsp} alt="">
        </a>
    </div>
</div>

<style>
    div{
        width: 100%;
        max-width: 300px;
        scroll-snap-align: center;
        display: flex;
        flex-direction: column;
        position: relative;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        padding: 5px;
        border-radius: 5px;
        box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
    }

    img{
        width:100%;
    }

    div:hover > h4{
        transform: translateX(155px);
    }

    h4{
        position: absolute;
        font-size: 20px;
        
        top: 15px;
        left: -150px;
        font-family: var(--secondaryFont);
        color: var(--negro);
        background-color: var(--amarillo);
        padding: 10px 10px 10px 50px;
        border-radius: 0px 10px 10px 0px;
        transition: all 450ms;
    }

    div.hoverCard{
        position: absolute;
        width: 340px;
        height: 75px;
        background-color: var(--blanco);
        bottom:-75px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        font-size: 20px;
        font-family: var(--primaryFont);
        transition: all 450ms;
        z-index: 0;
        padding: 15px;
        gap: 5px;
        
    }

    div:hover > div.hoverCard{
        transform: translateY(-75px);
    }

    a{
        width: 40%;
        font-size: 16px;
        display: flex;
        align-items: center;
        justify-content: flex-start;
        gap: 15px;
    }

    a img{
        width: 30px;
    }

</style>-->

<div class="profile_card">
    <img src={image} alt={name}>
    <div class="info" id="info">
        <ul class="social-icons">
            <li>
                <a href="/"><i class="fab fa-whatsapp"></i></a>
            </li>
        </ul>
        <h4 class="name">{name}</h4>
        <p class="price">${price}</p>
    </div>
</div>

<style>
    .profile_card {
    
    width: 100%;
    border-radius: 15px;
    overflow: hidden;
    position: relative;
    font-family: var(--secondaryFont);
    overflow: hidden;
}

.profile_card img {
    width: 100%;
}

.info {
    background: white;
    color: black;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    border-radius: 10px;
    padding-top: 10px;
    padding-bottom: 30px;
    transition: 0.5s ease;
}

.social-icons {
    display: flex;
    align-items: center;
    list-style: none;
    padding: 0;
    position: absolute;
    top: -50px;
    left: 0px;
}



.social-icons li {
    margin: 0 5px;
}

.social-icons li a {
    background: white;
    color: #25D366;
    height: 30px;
    width: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    border-radius: 5px;
    font-size: 25px;
}



.name {
    margin: 0;
    padding: 0 10px;
}

.price {
    margin: 0;
    padding: 0 10px;
    font-size: 16px;
}
</style>