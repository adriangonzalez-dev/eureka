<script>
    const derquiEmprende = 'img/derquiemprende.png'
    const mp = 'img/mp.png'
</script>

<section>
    <div class="feria">
        <p>Podes encontrarnos en Presidente Derqui participando de Derqui Emprende los viernes y sabados de 13 a 18hs</p>
        <a href="/"><img src={derquiEmprende} alt=""></a>
    </div>

    <div class="envio">
        <p>También podes realizarnos pedidos por whatsapp e instagram</p>
        <p>Aceptamos Mercado Pago</p><img src={mp} alt="">
    </div>
</section>

<style>

    section{
        display: flex;
        width: 80%;
        flex-direction: column;
        gap: 15px;
    }

    div.feria,div.envio{
        display: flex;
        width: 100%;
        flex-wrap: wrap;
        align-items: center;
        justify-content: center;
        font-family: var(--secondaryFont);
        font-size: 20px;
        font-weight: bold;
        text-align: center;
        
    }

    div.feria p{
        width: 100%;
    }

    div.feria a{
        width: 10%;
        
        min-width: 80px;
    }

    div.feria a img{
        width:100%;
        border-radius: 50%;
    }

    div.envio{
        flex-direction: column;
    }
    div.envio img{
        width:20%;
        
        min-width: 100px;
    }
</style>