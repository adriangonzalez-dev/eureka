<ul class="social-icons">
    <li>
        <a href="/"><i class="fab fa-whatsapp"></i></a>
    </li>
    <li>
        <a href="/"><i class="fab fa-instagram"></i></a>
    </li>
    <li>
        <a href="/"><i class="fab fa-twitter"></i></a>
    </li>
    <li>
        <a href="/"><i class="fab fa-snapchat"></i></a>
    </li>
</ul>

<style>
    .social-icons {
    display: flex;
    justify-content: center;
    list-style: none;
    z-index: 10;
}

.social-icons li {
    margin: 0 5px;
}

.social-icons li a {
    font-size: 20px;
    height: 40px;
    width: 40px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: white;
    position: relative;
    transition: 0.5s ease;
}

.social-icons li a:hover {
    background-image: linear-gradient(45deg, #12c2e9, #c471ed, #f64f59);
    background-clip: text;
    color: transparent;
    -webkit-text-fill-color: transparent;
    -webkit-background-clip: text;
    font-size: 25px;
}

.social-icons li a::before {
    content: '';
    position: absolute;
    z-index: -1;
    height: 40px;
    width: 40px;
    border-radius: 50%;
    background: linear-gradient(45deg, #12c2e9, #c471ed, #f64f59);
    transform: scale(1);
    transition: 0.5s ease-in-out;
}

.social-icons li a:hover::before {
    transform: scale(0);
}
</style>