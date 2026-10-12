<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>WebNova | Shop Smart</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,Helvetica,sans-serif;
}

html{
    scroll-behavior:smooth;
}

body{
    background:#f5f7fb;
    color:#172033;
    transition:.3s;
}

body.modal-open{
    overflow:hidden;
}

button,input,select{
    font:inherit;
}

button{
    cursor:pointer;
}

.topbar{
    background:#111a35;
    color:#fff;
    text-align:center;
    padding:9px;
    font-size:13px;
}

header{
    height:76px;
    background:#fff;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 6%;
    position:sticky;
    top:0;
    z-index:1000;
    box-shadow:0 2px 15px rgba(0,0,0,.08);
}

.logo{
    font-size:30px;
    font-weight:800;
    color:#315efb;
}

.logo span{
    color:#DA5508;
}

nav{
    display:flex;
    gap:26px;
}

nav a{
    text-decoration:none;
    color:#172033;
    font-weight:600;
}

nav a:hover{
    color:#315efb;
}

.header-actions{
    display:flex;
    align-items:center;
    gap:8px;
}

.header-actions button{
    border:0;
    background:#f0f3ff;
    width:42px;
    height:42px;
    border-radius:12px;
    font-size:18px;
}

.badge{
    background:#315efb;
    color:#fff;
    border-radius:50%;
    font-size:10px;
    padding:3px 6px;
    position:relative;
    top:-8px;
    left:-5px;
}

.hero{
    min-height:560px;
    padding:75px 7%;
    display:flex;
    align-items:center;
    justify-content:space-between;
    background:linear-gradient(120deg,#edf3ff,#f8f0ff);
    gap:50px;
}

.hero-content{
    max-width:590px;
}

.hero-small{
    color:#315efb;
    font-weight:bold;
    letter-spacing:2px;
    margin-bottom:15px;
}

.hero h1{
    font-size:60px;
    line-height:1.03;
    margin-bottom:20px;
}

.hero h1 span{
    color:#315efb;
}

.hero p{
    font-size:18px;
    color:#5d6678;
    line-height:1.7;
    margin-bottom:28px;
}

.hero-buttons{
    display:flex;
    gap:12px;
    margin-bottom:28px;
}

.primary-btn,.secondary-btn{
    padding:14px 25px;
    border-radius:11px;
    border:0;
    font-weight:bold;
}

.primary-btn{
    background:#315efb;
    color:#fff;
}

.secondary-btn{
    background:#fff;
    color:#315efb;
}

.hero-stats{
    display:flex;
    gap:28px;
}

.hero-stats div{
    display:flex;
    flex-direction:column;
}

.hero-stats strong{
    font-size:20px;
}

.hero-stats span{
    font-size:12px;
    color:#70798a;
    margin-top:4px;
}

.hero-image{
    width:470px;
    height:390px;
    border-radius:30px;
    overflow:hidden;
    box-shadow:0 20px 55px rgba(49,94,251,.22);
    position:relative;
}

.hero-image img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.hero-badge{
    position:absolute;
    right:18px;
    top:18px;
    background:#fff;
    padding:13px 16px;
    border-radius:14px;
    box-shadow:0 5px 20px rgba(0,0,0,.15);
    font-weight:bold;
}

.hero-badge span{
    color:#4D7DDD;
}

section{
    padding:65px 7%;
}

.section-heading{
    text-align:center;
    margin-bottom:35px;
}

.section-heading h2{
    font-size:35px;
    margin-bottom:8px;
}

.section-heading p{
    color:#6c7484;
}

.features{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
}

.feature{
    background:#fff;
    padding:27px 20px;
    border-radius:18px;
    text-align:center;
    box-shadow:0 5px 20px rgba(0,0,0,.05);
    transition:.3s;
}

.feature:hover{
    transform:translateY(-5px);
}

.feature-icon{
    font-size:35px; 
    margin-bottom:12px;
}

.feature h3{
    margin-bottom:8px;
}

.feature p{
    color:#70798a;
    font-size:14px;
    line-height:1.5;
}

.sale{
    background:linear-gradient(110deg,#315efb,#7c3aed);
    color:#FFF;
    border-radius:25px;
    padding:35px 40px;
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:25px;
}

.sale h2{
    font-size:32px;
    margin-bottom:8px;
}

.sale p{
    opacity:.9    ;
}

.countdown{
    display:flex;
    gap:10px;
}

.time-box{
    background:rgba(255,255,255,.16);
    border:1px solid rgba(255,255,255,.25);
    border-radius:12px;
    min-width:65px;
    padding:12px;
    text-align:center;
}

.time-box strong{
    display:block;
    font-size:23px;
}

.time-box span{
    font-size:10px;
}

.categories-grid{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
}

.category-card{
    height:220px;
    border-radius:20px;
    overflow:hidden;
    position:relative;
    cursor:pointer;
}

.category-card img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.4s;
}

.category-card:hover img{
    transform:scale(1.08);
}

.category-overlay{
    position:absolute;
    inset:0;
    background:linear-gradient(transparent,rgba(0,0,0,.75));
    display:flex;
    align-items:flex-end;
    padding:22px;
    color:#fff;
}

.category-overlay h3{
    font-size:22px;
}

.shop-controls{
    display:flex;
    justify-content:space-between;
    align-items:center;
    gap:12px;
    margin-bottom:22px;
    flex-wrap:wrap;
}

.search-box{
    flex:1;
    min-width:240px;
    display:flex;
    gap:8px;
}

.search-box input{
    width:100%;
    padding:15px 17px;
    border:1px solid #dce1ea;
    border-radius:12px;
    outline:none;
    background:#fff;
}

.image-search{
    padding:0 16px;
    border:0;
    border-radius:12px;
    background:#315efb;
    color:#fff;
    font-weight:bold;
}

.sort-box select{
    padding:14px 17px;
    border:1px solid #dce1ea;
    border-radius:12px;
    background:#fff;
}

.categories{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:30px;
}

.categories button{
    padding:10px 19px;
    border:0;
    border-radius:22px;
    background:#e9edf6;
    font-weight:600;
}

.categories button.active{
    background:#315efb;
    color:#fff;
}

.products{
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:22px;
}

.card{
    background:#fff;
    border-radius:18px;
    overflow:hidden;
    box-shadow:0 5px 18px rgba(0,0,0,.07);
    transition:.3s;
    position:relative;
}

.card:hover{
    transform:translateY(-7px);
    box-shadow:0 12px 28px rgba(0,0,0,.12);
}

.product-image{
    height:230px;
    position:relative;
    background:#f1f3f7;
    overflow:hidden;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.4s;
}

.card:hover .product-image img{
    transform:scale(1.06);
}

.wishlist{
    position:absolute;
    right:12px;
    top:12px;
    width:39px;
    height:39px;
    border:0;
    border-radius:50%;
    background:#fff;
    font-size:19px;
    box-shadow:0 3px 10px rgba(0,0,0,.12);
}

.wishlist.active{
    color:#e63946;
}

.discount{
    position:absolute;
    left:12px;
    top:12px;
    background:#16a34a;
    color:#fff;
    padding:6px 9px;
    border-radius:7px;
    font-size:11px;
    font-weight:bold;
}

.stock{
    color:#16a34a;
    font-size:12px;
    font-weight:bold;
    margin-bottom:7px;
}

.card-content{
    padding:17px;
}

.category-name{
    font-size:11px;
    color:#7c3aed;
    font-weight:bold;
    text-transform:uppercase;
    margin-bottom:7px;
}

.card h3{
    font-size:17px;
    margin-bottom:8px;
}

.brand{
    font-size:12px;
    color:#6b7280;
    margin-bottom:8px;
}

.rating{
    font-size:13px;
    color:#f59e0b;
    margin-bottom:10px;
}

.rating span{
    color:#747b88;
}

.price-row{
    display:flex;
    align-items:center;
    gap:9px;
    margin-bottom:8px;
}

.price{
    font-size:20px;
    font-weight:bold;
}

.old-price{
    text-decoration:line-through;
    color:#9299a6;
    font-size:13px;
}

.delivery{
    font-size:12px;
    color:#64748b;
    margin-bottom:13px;
}

.card-actions{
    display:flex;
    gap:7px;
}

.add-cart,.quick-view{
    flex:1;
    padding:10px;
    border-radius:9px;
    font-weight:bold;
}

.add-cart{
    border:0;
    background:#315efb;
    color:#fff;
}

.quick-view{
    border:1px solid #315efb;
    background:#fff;
    color:#315efb;
}

.no-products{
    text-align:center;
    grid-column:1/-1;
    padding:60px;
    color:#777;
}

.trending{
    background:#eef3ff;
}

.trending-grid{
    display:grid;
    grid-template-columns:1.2fr 1fr 1fr;
    gap:20px;
}

.trending-card{
    min-height:270px;
    border-radius:20px;
    overflow:hidden;
    position:relative;
}

.trending-card img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.trending-info{
    position:absolute;
    inset:0;
    padding:25px;
    display:flex;
    flex-direction:column;
    justify-content:flex-end;
    color:#fff;
    background:linear-gradient(transparent,rgba(0,0,0,.78));
}

.trending-info h3{
    font-size:25px;
    margin-bottom:7px;
}

.newsletter{
    background:#fff;
    border-radius:24px;
    padding:50px;
    text-align:center;
    box-shadow:0 5px 20px rgba(0,0,0,.05);
}

.newsletter h2{
    font-size:32px;
    margin-bottom:10px;
}

.newsletter p{
    color:#6c7484;
    margin-bottom:22px;
}

.newsletter-form{
    max-width:520px;
    margin:auto;
    display:flex;
    gap:8px;
}

.newsletter-form input{
    flex:1;
    padding:14px;
    border:1px solid #dce1ea;
    border-radius:10px;
    outline:none;
}

.newsletter-form button{
    border:0;
    background:#315efb;
    color:#fff;
    padding:0 20px;
    border-radius:10px;
    font-weight:bold;
}

.about{
    background:#111a35;
    color:#fff;
}

.about-container{
    max-width:850px;
    margin:auto;
    text-align:center;
}

.about h2{
    font-size:36px;
    margin-bottom:15px;
}

.about p{
    color:#cbd2e2;
    line-height:1.8;
}

footer{
    background:#0b1225;
    color:#fff;
    padding:35px 7%;
    text-align:center;
}

footer h2{
    color:#6d8cff;
    margin-bottom:8px;
}

footer p{
    color:#aeb7ca;
    margin:5px;
}

.cart-overlay{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.5);
    z-index:1999;
    display:none;
}

.cart-overlay.show{
    display:block;
}

.cart-panel{
    position:fixed;
    right:-430px;
    top:0;
    width:410px;
    height:100vh;
    background:#fff;
    z-index:2000;
    padding:25px;
    transition:.35s;
    overflow-y:auto;
}

.cart-panel.open{
    right:0;
}

.cart-header{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-bottom:25px;
}

.cart-header button{
    border:0;
    background:none;
    font-size:28px;
}

.cart-item{
    display:flex;
    gap:12px;
    padding:15px 0;
    border-bottom:1px solid #e5e7eb;
}

.cart-item img{
    width:75px;
    height:75px;
    object-fit:cover;
    border-radius:10px;
}

.cart-info{
    flex:1;
}

.cart-info h4{
    margin-bottom:5px;
}

.cart-price{
    font-weight:bold;
    margin-bottom:8px;
}

.quantity{
    display:flex;
    align-items:center;
    gap:8px;
}

.quantity button{
    width:27px;
    height:27px;
    border:0;
    background:#edf0f7;
    border-radius:6px;
}

.remove{
    margin-top:7px;
    border:0;
    background:none;
    color:#e63946;
    font-size:12px;
}

.cart-total{
    margin-top:25px;
    display:flex;
    justify-content:space-between;
    font-size:21px;
    font-weight:bold;
}

.checkout{
    width:100%;
    padding:14px;
    border:0;
    background:#315efb;
    color:#fff;
    border-radius:10px;
    margin-top:20px;
    font-weight:bold;
}

.empty-cart{
    text-align:center;
    padding:50px 10px;
    color:#777;
}

.modal{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.58);
    z-index:3000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:20px;
}

.modal.show{
    display:flex;
}

.modal-content{
    width:1000px;
    max-width:100%;
    background:#fff;
    border-radius:22px;
    overflow:hidden;
    display:grid;
    grid-template-columns:.9fr 1.1fr;
    position:relative;
    max-height:92vh;
}

.modal-image{
    height:620px;
}

.modal-image img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.modal-info{
    padding:38px;
    overflow-y:auto;
}

.modal-info h2{
    font-size:31px;
    margin:8px 0;
}

.modal-brand{
    color:#64748b;
    font-size:14px;
    margin-bottom:12px;
}

.modal-rating{
    margin-bottom:14px;
    color:#f59e0b;
}

.modal-rating span{
    color:#64748b;
}

.modal-description{
    color:#697386;
    line-height:1.7;
    margin:17px 0;
}

.modal-price{
    font-size:28px;
    font-weight:bold;
    margin:18px 0;
}

.modal-old-price{
    color:#9299a6;
    text-decoration:line-through;
    font-size:14px;
    margin-left:8px;
}

.modal-status{
    background:#ecfdf5;
    color:#15803d;
    padding:11px;
    border-radius:9px;
    font-size:13px;
    margin-bottom:18px;
}

.highlights h3,
.specifications h3{
    margin-bottom:12px;
}

.highlights ul{
    padding-left:20px;
    color:#5f697b;
    line-height:1.8;
    margin-bottom:20px;
}

.specifications{
    margin-top:20px;
}

.spec-row{
    display:flex;
    justify-content:space-between;
    gap:20px;
    padding:9px 0;
    border-bottom:1px solid #e7eaf0;
    font-size:13px;
}

.spec-row span:first-child{
    color:#6b7280;
}

.spec-row span:last-child{
    font-weight:bold;
    text-align:right;
}

.seller{
    margin-top:20px;
    background:#f5f7fb;
    padding:14px;
    border-radius:10px;
    font-size:13px;
}

.close-modal{
    position:absolute;
    right:15px;
    top:12px;
    width:40px;
    height:40px;
    border:0;
    border-radius:50%;
    background:#fff;
    font-size:25px;
    z-index:5;
}

.modal-cart{
    width:100%;
    padding:14px;
    border:0;
    background:#315efb;
    color:#fff;
    border-radius:10px;
    font-weight:bold;
    margin-top:18px;
}

.image-modal-content{
    width:450px;
    max-width:100%;
    background:#fff;
    border-radius:20px;
    padding:30px;
    text-align:center;
    position:relative;
}

.image-modal-content h2{
    margin-bottom:10px;
}

.image-modal-content p{
    color:#697386;
    line-height:1.6;
    margin-bottom:20px;
}

.image-upload{
    border:2px dashed #315efb;
    border-radius:16px;
    padding:35px 20px;
    margin:20px 0;
}

.image-upload label{
    display:inline-block;
    padding:12px 20px;
    background:#315efb;
    color:#fff;
    border-radius:9px;
    font-weight:bold;
}

.image-preview{
    max-width:100%;
    max-height:180px;
    border-radius:12px;
    display:none;
    margin:15px auto;
}

.toast{
    position:fixed;
    right:25px;
    bottom:25px;
    background:#172033;
    color:#fff;
    padding:14px 20px;
    border-radius:10px;
    z-index:5000;
    transform:translateY(100px);
    opacity:0;
    transition:.3s;
}

.toast.show{
    transform:translateY(0);
    opacity:1;
}

.dark{
    background:#101522;
    color:#f5f7fb;
}

.dark header,
.dark .feature,
.dark .card,
.dark .newsletter,
.dark .cart-panel,
.dark .modal-content,
.dark .image-modal-content{
    background:#182033;
    color:#fff;
}

.dark nav a{
    color:#fff;
}

.dark .header-actions button{
    background:#273149;
    color:#fff;
}

.dark .hero{
    background:linear-gradient(120deg,#141c32,#251b3d);
}

.dark .hero p,
.dark .section-heading p,
.dark .feature p,
.dark .newsletter p,
.dark .delivery,
.dark .brand,
.dark .modal-brand,
.dark .modal-description{
    color:#bdc6d8;
}

.dark .search-box input,
.dark .sort-box select,
.dark .newsletter-form input{
    background:#222b40;
    color:#fff;
    border-color:#3b465e;
}

.dark .categories button{
    background:#29344b;
    color:#fff;
}

.dark .categories button.active{
    background:#315efb;
}

.dark .product-image{
    background:#222b40;
}

.dark .quick-view{
    background:#182033;
}

.dark .seller{
    background:#222b40;
}

.dark .spec-row{
    border-color:#3b465e;
}

.dark .spec-row span:first-child{
    color:#bdc6d8;
}

@media(max-width:1100px){

    .products{
        grid-template-columns:repeat(3,1fr);
    }

    .features{
        grid-template-columns:repeat(2,1fr);
    }

    .categories-grid{
        grid-template-columns:repeat(2,1fr);
    }
}

@media(max-width:850px){

    nav{
        display:none;
    }

    .hero{
        flex-direction:column;
        text-align:center;
    }

    .hero h1{
        font-size:46px;
    }

    .hero-buttons{
        justify-content:center;
    }

    .hero-stats{
        justify-content:center;
    }

    .hero-image{
        width:100%;
        max-width:500px;
    }

    .products{
        grid-template-columns:repeat(2,1fr);
    }

    .trending-grid{
        grid-template-columns:1fr 1fr;
    }

    .sale{
        flex-direction:column;
        text-align:center;
    }

    .modal-content{
        grid-template-columns:1fr;
        max-height:90vh;
        overflow:auto;
    }

    .modal-image{
        height:300px;
    }

    .modal-info{
        overflow-y:visible;
    }
}

@media(max-width:550px){

    header{
        padding:0 4%;
    }

    .logo{
        font-size:24px;
    }

    .header-actions button{
        width:36px;
        height:36px;
    }

    section{
        padding:45px 5%;
    }

    .hero{
        padding:55px 5%;
    }

    .hero h1{
        font-size:37px;
    }

    .hero-stats{
        gap:15px;
    }

    .features,
    .categories-grid,
    .products,
    .trending-grid{
        grid-template-columns:1fr;
    }

    .category-card{
        height:250px;
    }

    .product-image{
        height:270px;
    }

    .cart-panel{
        width:100%;
    }

    .newsletter{
        padding:35px 20px;
    }

    .newsletter-form{
        flex-direction:column;
    }

    .newsletter-form button{
        padding:13px;
    }

    .search-box{
        flex-direction:column;
    }

    .image-search{
        padding:13px;
    }

    .hero-buttons{
        flex-direction:column;
    }

    .hero-buttons button{
        width:100%;
    }

    .countdown{
        width:100%;
        justify-content:center;
    }

    .time-box{
        min-width:58px;
    }

    .modal{
        padding:10px;
    }

    .modal-content{
        max-height:95vh;
        border-radius:16px;
    }

    .modal-image{
        height:250px;
    }

    .modal-info{
        padding:25px 20px;
    }

    .modal-info h2{
        font-size:25px;
    }
}
</style>
</head>

<body>

<div class="topbar">
    ⚡ Flash Sale is Live — Extra discounts on selected products today!
</div>

<header>

    <div class="logo">
        Web<span>Nova</span>
    </div>

    <nav>
        <a href="#home">Home</a>
        <a href="#shop">Shop</a>
        <a href="#categories">Categories</a>
        <a href="#trending">Trending</a>
        <a href="#about">About</a>
    </nav>

    <div class="header-actions">
        <button onclick="toggleDark()">🌙</button>
        <button onclick="showWishlist()">♡<span class="badge" id="wishCount">0</span></button>
        <button onclick="openCart()">🛒<span class="badge" id="cartCount">0</span></button>
    </div>

</header>

<section class="hero" id="home">

    <div class="hero-content">

        <div class="hero-small">
            WELCOME TO WEBNOVA
        </div>

        <h1>
            Discover. <span>Shop.</span> Enjoy.
        </h1>

        <p>
            Explore trending products, discover exclusive deals and enjoy a modern interactive shopping experience designed with WebNova.
        </p>

        <div class="hero-buttons">
            <button class="primary-btn" onclick="document.getElementById('shop').scrollIntoView()">
                Shop Now
            </button>

            <button class="secondary-btn" onclick="document.getElementById('categories').scrollIntoView()">
                Explore Categories
            </button>
        </div>

        <div class="hero-stats">

            <div>
                <strong>10K+</strong>
                <span>Products</span>
            </div>

            <div>
                <strong>50K+</strong>
                <span>Happy Users</span>
            </div>

            <div>
                <strong>4.8★</strong>
                <span>Customer Rating</span>
            </div>

        </div>

    </div>

    <div class="hero-image">

        <img src="https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?auto=format&fit=crop&w=1000&q=90">

        <div class="hero-badge">
            Up to <span>50% OFF</span>
        </div>

    </div>

</section>

<section>

    <div class="features">

        <div class="feature">
            <div class="feature-icon">🚚</div>
            <h3>Fast Delivery</h3>
            <p>Quick and reliable delivery experience.</p>
        </div>

        <div class="feature">
            <div class="feature-icon">🔒</div>
            <h3>Secure Shopping</h3>
            <p>Designed with a safe shopping experience.</p>
        </div>

        <div class="feature">
            <div class="feature-icon">↩️</div>
            <h3>Easy Returns</h3>
            <p>Simple return experience for eligible products.</p>
        </div>

        <div class="feature">
            <div class="feature-icon">⭐</div>
            <h3>Top Quality</h3>
            <p>Discover products across popular categories.</p>
        </div>

    </div>

</section>

<section>

    <div class="sale">

        <div>
            <h2>🔥 Mega Flash Sale</h2>
            <p>Limited-time deals are waiting for you.</p>
        </div>

        <div class="countdown">

            <div class="time-box">
                <strong id="hours">14</strong>
                <span>HOURS</span>
            </div>

            <div class="time-box">
                <strong id="minutes">30</strong>
                <span>MINUTES</span>
            </div>

            <div class="time-box">
                <strong id="seconds">00</strong>
                <span>SECONDS</span>
            </div>

        </div>

    </div>

</section>

<section id="categories">

    <div class="section-heading">
        <h2>Shop by Category</h2>
        <p>Explore products from your favorite categories</p>
    </div>

    <div class="categories-grid">

        <div class="category-card" onclick="selectCategory('Electronics')">
            <img src="https://images.unsplash.com/photo-1498049794561-7780e7231661?auto=format&fit=crop&w=700&q=85">
            <div class="category-overlay">
                <h3>Electronics</h3>
            </div>
        </div>

        <div class="category-card" onclick="selectCategory('Fashion')">
            <img src="https://images.unsplash.com/photo-1445205170230-053b83016050?auto=format&fit=crop&w=700&q=85">
            <div class="category-overlay">
                <h3>Fashion</h3>
            </div>
        </div>

        <div class="category-card" onclick="selectCategory('Home')">
            <img src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3?auto=format&fit=crop&w=700&q=85">
            <div class="category-overlay">
                <h3>Home</h3>
            </div>
        </div>

        <div class="category-card" onclick="selectCategory('Sports')">
            <img src="https://images.unsplash.com/photo-1517836357463-d25dfeac3438?auto=format&fit=crop&w=700&q=85">
            <div class="category-overlay">
                <h3>Sports</h3>
            </div>
        </div>

    </div>

</section>

<section id="shop">

    <div class="section-heading">
        <h2>Explore Products</h2>
        <p>Find products that match your style and needs</p>
    </div>

    <div class="shop-controls">

        <div class="search-box">

            <input
                type="text"
                id="search"
                placeholder="Search products..."
                oninput="displayProducts()"
            >

            <button class="image-search" onclick="openImageSearch()">
                📷 Search by Image
            </button>

        </div>

        <div class="sort-box">

            <select id="sort" onchange="displayProducts()">
                <option value="default">Sort Products</option>
                <option value="low">Price: Low to High</option>
                <option value="high">Price: High to Low</option>
                <option value="rating">Highest Rated</option>
            </select>

        </div>

    </div>

    <div class="categories">

        <button class="active" onclick="filterProducts('All',this)">
            All
        </button>

        <button onclick="filterProducts('Electronics',this)">
            Electronics
        </button>

        <button onclick="filterProducts('Fashion',this)">
            Fashion
        </button>

        <button onclick="filterProducts('Home',this)">
            Home
        </button>

        <button onclick="filterProducts('Beauty',this)">
            Beauty
        </button>

        <button onclick="filterProducts('Sports',this)">
            Sports
        </button>

    </div>

    <div class="products" id="products"></div>

</section>

<section class="trending" id="trending">

    <div class="section-heading">
        <h2>🔥 Trending Now</h2>
        <p>Popular picks people are exploring right now</p>
    </div>

    <div class="trending-grid">

        <div class="trending-card">
            <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=900&q=85">

            <div class="trending-info">
                <h3>Premium Audio</h3>
                <p>Immersive sound for every moment</p>
            </div>
        </div>

        <div class="trending-card">
            <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=700&q=85">

            <div class="trending-info">
                <h3>Street Style</h3>
                <p>Step into the latest trends</p>
            </div>
        </div>

        <div class="trending-card">
            <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=700&q=85">

            <div class="trending-info">
                <h3>Smart Life</h3>
                <p>Technology for everyday living</p>
            </div>
        </div>

    </div>

</section>

<section>

    <div class="newsletter">

        <h2>Stay in the WebNova Loop ✨</h2>

        <p>
            Get updates about new products, exclusive deals and special offers.
        </p>

        <div class="newsletter-form">

            <input
                type="email"
                id="email"
                placeholder="Enter your email"
            >

            <button onclick="subscribe()">
                Subscribe
            </button>

        </div>

    </div>

</section>

<section class="about" id="about">

    <div class="about-container">

        <h2>About WebNova</h2>

        <p>
            WebNova is a modern e-commerce website prototype developed using HTML, CSS and JavaScript. It demonstrates product discovery, category filtering, search, sorting, wishlist management, image search interface, detailed product information, shopping cart functionality, responsive design and interactive user experiences.
        </p>

    </div>

</section>

<footer>

    <h2>WebNova</h2>

    <p>Online Shopping Website Prototype</p>
    <p>HTML • CSS • JavaScript</p>
    <p>© 2026 WebNova</p>

</footer>

<div class="cart-overlay" id="cartOverlay" onclick="closeCart()"></div>

<div class="cart-panel" id="cartPanel">

    <div class="cart-header">
        <h2>Shopping Cart</h2>
        <button onclick="closeCart()">×</button>
    </div>

    <div id="cartItems"></div>

    <div class="cart-total">
        <span>Total</span>
        <span>₹<span id="total">0</span></span>
    </div>

    <button class="checkout" onclick="checkout()">
        Proceed to Checkout
    </button>

</div>

<div class="modal" id="productModal">

    <div class="modal-content">

        <button class="close-modal" onclick="closeModal()">
            ×
        </button>

        <div class="modal-image">
            <img id="modalImage">
        </div>

        <div class="modal-info">

            <div class="category-name" id="modalCategory"></div>

            <h2 id="modalName"></h2>

            <div class="modal-brand" id="modalBrand"></div>

            <div class="modal-rating" id="modalRating"></div>

            <p class="modal-description" id="modalDescription"></p>

            <div class="modal-price">

                ₹<span id="modalPrice"></span>

                <span class="modal-old-price" id="modalOldPrice"></span>

            </div>

            <div class="modal-status" id="modalStock"></div>

            <div class="highlights">

                <h3>Product Highlights</h3>

                <ul id="modalHighlights"></ul>

            </div>

            <div class="specifications">

                <h3>Specifications</h3>

                <div id="modalSpecs"></div>

            </div>

            <div class="seller" id="modalSeller"></div>

            <button class="modal-cart" id="modalCart">
                Add to Cart
            </button>

        </div>

    </div>

</div>

<div class="modal" id="imageModal">

    <div class="image-modal-content">

        <button class="close-modal" onclick="closeImageSearch()">
            ×
        </button>

        <h2>📷 Search by Image</h2>

        <p>
            Select a product image from your device to preview it.
        </p>

        <div class="image-upload">

            <label for="imageInput">
                Choose Image
            </label>

            <input
                type="file"
                id="imageInput"
                accept="image/*"
                hidden
                onchange="previewImage(event)"
            >

            <img
                class="image-preview"
                id="imagePreview"
            >

        </div>

        <button class="primary-btn" onclick="imageSearchResult()">
            Find Similar Products
        </button>

    </div>

</div>

<div class="toast" id="toast"></div>

<script>
const products=[
{
id:1,
name:"Apple AirPods Pro",
brand:"Apple",
category:"Electronics",
price:24900,
oldPrice:26900,
rating:4.8,
reviews:1284,
discount:"8% OFF",
stock:"In Stock • 12 units left",
delivery:"Free delivery by Tomorrow",
seller:"WebNova Electronics • 98% positive ratings",
image:"https://images.unsplash.com/photo-1606220945770-b5b6c2c55bf1?auto=format&fit=crop&w=700&q=85",
description:"Premium wireless earbuds with immersive sound, active noise cancellation and a comfortable design for music, calls and everyday use.",
highlights:[
"Active Noise Cancellation",
"Adaptive Transparency Mode",
"MagSafe Charging Case",
"Sweat and water resistant",
"High-quality wireless audio"
],
specs:{
"Connectivity":"Bluetooth",
"Battery":"Up to 6 hours",
"Charging":"USB-C / MagSafe",
"Water Resistance":"IPX4",
"Type":"Wireless Earbuds"
}
},
{
id:2,
name:"Smart Watch Series",
brand:"NovaTech",
category:"Electronics",
price:3999,
oldPrice:5999,
rating:4.5,
reviews:862,
discount:"33% OFF",
stock:"In Stock • 24 units left",
delivery:"Free delivery in 2 days",
seller:"WebNova Gadgets • 96% positive ratings",
image:"https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=700&q=85",
description:"Modern smartwatch with fitness tracking, health monitoring, notifications and a stylish display for everyday life.",
highlights:[
"Heart-rate monitoring",
"Daily activity tracking",
"Call and message alerts",
"Multiple watch faces",
"Long-lasting battery"
],
specs:{
"Display":"AMOLED",
"Battery":"Up to 7 days",
"Connectivity":"Bluetooth 5.3",
"Water Resistance":"5 ATM",
"Compatibility":"Android & iOS"
}
},
{
id:3,
name:"Premium Headphones",
brand:"SoundMax",
category:"Electronics",
price:5999,
oldPrice:7999,
rating:4.7,
reviews:934,
discount:"25% OFF",
stock:"In Stock • 18 units left",
delivery:"Free delivery by Tomorrow",
seller:"SoundMax Official • 97% positive ratings",
image:"https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=700&q=85",
description:"Over-ear wireless headphones designed for rich audio, deep bass and comfortable long listening sessions.",
highlights:[
"Active Noise Cancellation",
"Deep Bass Audio",
"40-hour battery",
"Built-in microphone",
"Comfort-fit ear cushions"
],
specs:{
"Driver":"40mm",
"Battery":"40 hours",
"Connectivity":"Bluetooth 5.2",
"Charging":"USB-C",
"Weight":"265g"
}
},
{
id:4,
name:"Classic Sneakers",
brand:"UrbanStep",
category:"Fashion",
price:2499,
oldPrice:3999,
rating:4.6,
reviews:741,
discount:"37% OFF",
stock:"In Stock • Multiple sizes",
delivery:"Free delivery in 2 days",
seller:"UrbanStep Store • 95% positive ratings",
image:"https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=700&q=85",
description:"Comfortable everyday sneakers with a modern design, cushioned sole and lightweight construction.",
highlights:[
"Lightweight construction",
"Cushioned sole",
"Breathable upper",
"Everyday casual design",
"Durable outsole"
],
specs:{
"Material":"Synthetic & Mesh",
"Sole":"Rubber",
"Closure":"Lace-up",
"Use":"Casual",
"Gender":"Unisex"
}
},
{
id:5,
name:"Premium Sunglasses",
brand:"VisionPro",
category:"Fashion",
price:1799,
oldPrice:2999,
rating:4.4,
reviews:528,
discount:"40% OFF",
stock:"In Stock • 32 units left",
delivery:"Free delivery in 3 days",
seller:"VisionPro Official • 94% positive ratings",
image:"https://images.unsplash.com/photo-1511499767150-a48a237f0083?auto=format&fit=crop&w=700&q=85",
description:"Stylish sunglasses with a timeless frame designed for everyday fashion and comfortable outdoor use.",
highlights:[
"UV protection",
"Lightweight frame",
"Classic design",
"Scratch-resistant lenses",
"Comfortable nose pads"
],
specs:{
"Lens":"Polarized",
"Protection":"UV400",
"Frame":"Acetate",
"Style":"Classic",
"Use":"Outdoor"
}
},
{
id:6,
name:"Leather Backpack",
brand:"UrbanCarry",
category:"Fashion",
price:2899,
oldPrice:4499,
rating:4.5,
reviews:653,
discount:"35% OFF",
stock:"In Stock • 15 units left",
delivery:"Free delivery in 2 days",
seller:"UrbanCarry • 96% positive ratings",
image:"https://images.unsplash.com/photo-1553062407-98eeb64c6a62?auto=format&fit=crop&w=700&q=85",
description:"Spacious and stylish backpack suitable for college, work and travel with organized storage compartments.",
highlights:[
"Large main compartment",
"Laptop sleeve",
"Water-resistant exterior",
"Multiple pockets",
"Comfortable shoulder straps"
],
specs:{
"Material":"Faux Leather",
"Capacity":"22 Litres",
"Laptop Support":"Up to 15.6 inch",
"Closure":"Zip",
"Use":"College / Travel"
}
},
{
id:7,
name:"Modern Table Lamp",
brand:"LumaHome",
category:"Home",
price:1299,
oldPrice:1999,
rating:4.3,
reviews:412,
discount:"35% OFF",
stock:"In Stock • 20 units left",
delivery:"Free delivery in 3 days",
seller:"LumaHome • 93% positive ratings",
image:"https://images.unsplash.com/photo-1507473885765-e6ed057f782c?auto=format&fit=crop&w=700&q=85",
description:"Minimal modern table lamp that adds a warm and elegant look to bedrooms, desks and living spaces.",
highlights:[
"Warm ambient lighting",
"Modern minimalist design",
"Energy efficient",
"Compact footprint",
"Suitable for desk or bedside"
],
specs:{
"Light Type":"LED",
"Power":"8W",
"Color Temperature":"Warm White",
"Material":"Metal & Glass",
"Control":"Switch"
}
},
{
id:8,
name:"Modern Chair",
brand:"HomeCraft",
category:"Home",
price:5499,
oldPrice:6999,
rating:4.6,
reviews:388,
discount:"21% OFF",
stock:"In Stock • 8 units left",
delivery:"Free delivery in 4 days",
seller:"HomeCraft Furniture • 95% positive ratings",
image:"https://images.unsplash.com/photo-1503602642458-232111445657?auto=format&fit=crop&w=700&q=85",
description:"Comfortable modern chair with a clean design suitable for home, study rooms or workspace environments.",
highlights:[
"Ergonomic back support",
"Soft cushioned seat",
"Strong frame",
"Modern design",
"Easy maintenance"
],
specs:{
"Material":"Fabric & Wood",
"Frame":"Solid Wood",
"Seating":"Single",
"Use":"Home / Office",
"Assembly":"Required"
}
},
{
id:9,
name:"Ceramic Coffee Set",
brand:"CasaLiving",
category:"Home",
price:899,
oldPrice:1299,
rating:4.2,
reviews:296,
discount:"30% OFF",
stock:"In Stock • 40 sets left",
delivery:"Free delivery in 3 days",
seller:"CasaLiving • 92% positive ratings",
image:"https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd?auto=format&fit=crop&w=700&q=85",
description:"Elegant ceramic coffee set designed for everyday use, gatherings and special occasions.",
highlights:[
"Premium ceramic finish",
"Easy to clean",
"Elegant design",
"Suitable for hot beverages",
"Gift-friendly packaging"
],
specs:{
"Material":"Ceramic",
"Pieces":"6",
"Capacity":"250ml each",
"Microwave Safe":"Yes",
"Dishwasher Safe":"Yes"
}
},
{
id:10,
name:"Luxury Perfume",
brand:"Aurelia",
category:"Beauty",
price:3299,
oldPrice:4999,
rating:4.7,
reviews:721,
discount:"34% OFF",
stock:"In Stock • 18 units left",
delivery:"Free delivery in 2 days",
seller:"Aurelia Beauty • 97% positive ratings",
image:"https://images.unsplash.com/photo-1541643600914-78b084683601?auto=format&fit=crop&w=700&q=85",
description:"A sophisticated fragrance with a premium aroma designed for everyday wear and special occasions.",
highlights:[
"Long-lasting fragrance",
"Elegant floral notes",
"Premium glass bottle",
"Suitable for special occasions",
"Gift-ready packaging"
],
specs:{
"Volume":"100ml",
"Fragrance":"Eau de Parfum",
"Family":"Floral",
"Longevity":"8–10 hours",
"Gender":"Unisex"
}
},
{
id:11,
name:"Skincare Essentials",
brand:"GlowCare",
category:"Beauty",
price:1599,
oldPrice:2299,
rating:4.4,
reviews:634,
discount:"30% OFF",
stock:"In Stock • 25 kits left",
delivery:"Free delivery in 3 days",
seller:"GlowCare Official • 95% positive ratings",
image:"https://images.unsplash.com/photo-1556229010-6c3f2c9ca5f8?auto=format&fit=crop&w=700&q=85",
description:"A collection of everyday skincare essentials designed for a simple and refreshing personal-care routine.",
highlights:[
"Daily cleansing",
"Hydration support",
"Gentle formula",
"Travel-friendly sizes",
"Simple skincare routine"
],
specs:{
"Skin Type":"Normal / Combination",
"Kit Type":"Daily Care",
"Items":"4",
"Fragrance":"Mild",
"Suitable For":"Adults"
}
},
{
id:12,
name:"Makeup Collection",
brand:"BeautyNova",
category:"Beauty",
price:2199,
oldPrice:3499,
rating:4.5,
reviews:547,
discount:"37% OFF",
stock:"In Stock • 16 kits left",
delivery:"Free delivery in 3 days",
seller:"BeautyNova Store • 94% positive ratings",
image:"https://images.unsplash.com/photo-1596462502278-27bfdc403348?auto=format&fit=crop&w=700&q=85",
description:"A versatile makeup collection containing everyday beauty essentials for creating different looks.",
highlights:[
"Multiple shades",
"Everyday essentials",
"Compact packaging",
"Easy application",
"Suitable for different looks"
],
specs:{
"Kit Type":"Makeup Set",
"Items":"8",
"Finish":"Mixed",
"Use":"Daily / Party",
"Packaging":"Compact"
}
},
{
id:13,
name:"Premium Yoga Mat",
brand:"FlexFit",
category:"Sports",
price:999,
oldPrice:1499,
rating:4.5,
reviews:853,
discount:"33% OFF",
stock:"In Stock • 35 units left",
delivery:"Free delivery in 2 days",
seller:"FlexFit Sports • 96% positive ratings",
image:"https://images.unsplash.com/photo-1592432678016-e910b452f9a2?auto=format&fit=crop&w=700&q=85",
description:"Comfortable non-slip yoga mat suitable for yoga, stretching, meditation and home workouts.",
highlights:[
"Non-slip surface",
"Comfortable cushioning",
"Lightweight",
"Easy to carry",
"Moisture resistant"
],
specs:{
"Thickness":"6mm",
"Material":"TPE",
"Length":"183cm",
"Width":"61cm",
"Type":"Exercise Mat"
}
},
{
id:14,
name:"Fitness Dumbbells",
brand:"PowerZone",
category:"Sports",
price:1999,
oldPrice:2799,
rating:4.6,
reviews:462,
discount:"29% OFF",
stock:"In Stock • 10 sets left",
delivery:"Free delivery in 3 days",
seller:"PowerZone Fitness • 97% positive ratings",
image:"https://images.unsplash.com/photo-1583454110551-21f2fa2afe61?auto=format&fit=crop&w=700&q=85",
description:"Durable dumbbells designed for strength training, muscle development and home fitness routines.",
highlights:[
"Non-slip grip",
"Durable construction",
"Compact design",
"Suitable for home workouts",
"Multiple exercise options"
],
specs:{
"Total Weight":"10kg",
"Material":"Cast Iron",
"Grip":"Textured",
"Set":"2 Dumbbells",
"Use":"Strength Training"
}
},
{
id:15,
name:"Running Shoes Pro",
brand:"RunX",
category:"Sports",
price:2999,
oldPrice:4499,
rating:4.8,
reviews:1025,
discount:"33% OFF",
stock:"In Stock • Multiple sizes",
delivery:"Free delivery in 2 days",
seller:"RunX Official • 98% positive ratings",
image:"https://images.unsplash.com/photo-1551107696-a4b0c5a0d9a2?auto=format&fit=crop&w=700&q=85",
description:"Lightweight running shoes designed for comfort, movement, daily training and active lifestyles.",
highlights:[
"Lightweight build",
"Cushioned midsole",
"Breathable mesh",
"Flexible outsole",
"Impact protection"
],
specs:{
"Upper":"Breathable Mesh",
"Sole":"Rubber",
"Closure":"Lace-up",
"Use":"Running / Training",
"Fit":"Regular"
}
},
{
id:16,
name:"Travel Water Bottle",
brand:"HydroNova",
category:"Sports",
price:699,
oldPrice:999,
rating:4.3,
reviews:375,
discount:"30% OFF",
stock:"In Stock • 50 units left",
delivery:"Free delivery in 3 days",
seller:"HydroNova • 95% positive ratings",
image:"https://images.unsplash.com/photo-1602143407151-7111542de6e8?auto=format&fit=crop&w=700&q=85",
description:"Reusable travel bottle with a practical design for workouts, travel, college and everyday hydration.",
highlights:[
"Leak-resistant lid",
"Reusable design",
"Lightweight body",
"Easy-grip shape",
"Travel friendly"
],
specs:{
"Capacity":"750ml",
"Material":"BPA-free Plastic",
"Cap":"Leak Resistant",
"Use":"Travel / Fitness",
"Weight":"180g"
}
}
];

let currentCategory="All";
let cart=[];
let wishlist=[];

function displayProducts(){

    let container=document.getElementById("products");
    let search=document.getElementById("search").value.toLowerCase();
    let sort=document.getElementById("sort").value;

    let filtered=products.filter(product=>{

        let categoryMatch=
            currentCategory==="All" ||
            product.category===currentCategory;

        let searchMatch=
            product.name.toLowerCase().includes(search) ||
            product.category.toLowerCase().includes(search) ||
            product.brand.toLowerCase().includes(search);

        return categoryMatch&&searchMatch;
    });

    if(sort==="low"){
        filtered.sort((a,b)=>a.price-b.price);
    }

    if(sort==="high"){
        filtered.sort((a,b)=>b.price-a.price);
    }

    if(sort==="rating"){
        filtered.sort((a,b)=>b.rating-a.rating);
    }

    container.innerHTML="";

    if(filtered.length===0){

        container.innerHTML=
            '<div class="no-products">No products found. Try another search.</div>';

        return;
    }

    filtered.forEach(product=>{

        let liked=wishlist.includes(product.id);

        container.innerHTML+=`

        <div class="card">

            <div class="product-image">

                <img src="${product.image}" alt="${product.name}">

                <div class="discount">
                    ${product.discount}
                </div>

                <button
                    class="wishlist ${liked?"active":""}"
                    onclick="addWishlist(${product.id})"
                >
                    ${liked?"♥":"♡"}
                </button>

            </div>

            <div class="card-content">

                <div class="category-name">
                    ${product.category}
                </div>

                <h3>
                    ${product.name}
                </h3>

                <div class="brand">
                    Brand: ${product.brand}
                </div>

                <div class="stock">
                    ${product.stock}
                </div>

                <div class="rating">
                    ★★★★★
                    <span>
                        ${product.rating}
                        (${product.reviews.toLocaleString()} reviews)
                    </span>
                </div>

                <div class="price-row">

                    <div class="price">
                        ₹${product.price.toLocaleString()}
                    </div>

                    <div class="old-price">
                        ₹${product.oldPrice.toLocaleString()}
                    </div>

                </div>

                <div class="delivery">
                    🚚 ${product.delivery}
                </div>

                <div class="card-actions">

                    <button
                        class="quick-view"
                        onclick="openProduct(${product.id})"
                    >
                        View Details
                    </button>

                    <button
                        class="add-cart"
                        onclick="addToCart(${product.id})"
                    >
                        Add Cart
                    </button>

                </div>

            </div>

        </div>

        `;
    });
}

function filterProducts(category,button){

    currentCategory=category;

    document.querySelectorAll(".categories button").forEach(btn=>{
        btn.classList.remove("active");
    });

    button.classList.add("active");

    displayProducts();
}

function selectCategory(category){

    currentCategory=category;

    document.getElementById("shop").scrollIntoView();

    document.querySelectorAll(".categories button").forEach(btn=>{
        btn.classList.toggle(
            "active",
            btn.textContent===category
        );
    });

    displayProducts();
}

function addToCart(id){

    let item=cart.find(product=>product.id===id);

    if(item){
        item.quantity++;
    }else{
        cart.push({
            id:id,
            quantity:1
        });
    }

    updateCart();

    showToast("Product added to cart 🛒");
}

function updateCart(){

    let count=cart.reduce(
        (total,item)=>total+item.quantity,
        0
    );

    document.getElementById("cartCount").textContent=count;

    let container=document.getElementById("cartItems");

    container.innerHTML="";

    if(cart.length===0){

        container.innerHTML=
            '<div class="empty-cart"><div style="font-size:55px">🛒</div><p>Your cart is empty.</p></div>';

        document.getElementById("total").textContent="0";

        return;
    }

    let total=0;

    cart.forEach(item=>{

        let product=products.find(
            product=>product.id===item.id
        );

        total+=product.price*item.quantity;

        container.innerHTML+=`

        <div class="cart-item">

            <img src="${product.image}">

            <div class="cart-info">

                <h4>
                    ${product.name}
                </h4>

                <div class="cart-price">
                    ₹${product.price.toLocaleString()}
                </div>

                <div class="quantity">

                    <button
                        onclick="changeQuantity(${product.id},-1)"
                    >
                        −
                    </button>

                    <span>
                        ${item.quantity}
                    </span>

                    <button
                        onclick="changeQuantity(${product.id},1)"
                    >
                        +
                    </button>

                </div>

                <button
                    class="remove"
                    onclick="removeFromCart(${product.id})"
                >
                    Remove
                </button>

            </div>

        </div>

        `;
    });

    document.getElementById("total").textContent=
        total.toLocaleString();
}

function changeQuantity(id,value){

    let item=cart.find(
        product=>product.id===id
    );

    if(item){

        item.quantity+=value;

        if(item.quantity<=0){

            cart=cart.filter(
                product=>product.id!==id
            );

        }
    }

    updateCart();
}

function removeFromCart(id){

    cart=cart.filter(
        product=>product.id!==id
    );

    updateCart();

    showToast("Product removed");
}

function addWishlist(id){

    if(wishlist.includes(id)){

        wishlist=wishlist.filter(
            product=>product!==id
        );

        showToast("Removed from wishlist");

    }else{

        wishlist.push(id);

        showToast("Added to wishlist ❤️");
    }

    document.getElementById("wishCount").textContent=
        wishlist.length;

    displayProducts();
}

function showWishlist(){

    if(wishlist.length===0){

        showToast("Your wishlist is empty");

        return;
    }

    let names=wishlist.map(id=>{

        let product=products.find(
            product=>product.id===id
        );

        return product.name;
    });

    alert(
        "Your Wishlist\n\n"+
        names.join("\n")
    );
}

function openCart(){

    document.getElementById("cartPanel")
        .classList.add("open");

    document.getElementById("cartOverlay")
        .classList.add("show");

    document.body.classList.add("modal-open");
}

function closeCart(){

    document.getElementById("cartPanel")
        .classList.remove("open");

    document.getElementById("cartOverlay")
        .classList.remove("show");

    if(!document.getElementById("productModal").classList.contains("show") &&
       !document.getElementById("imageModal").classList.contains("show")){

        document.body.classList.remove("modal-open");
    }
}

function openProduct(id){

    let product=products.find(
        product=>product.id===id
    );

    document.getElementById("modalImage").src=
        product.image;

    document.getElementById("modalCategory").textContent=
        product.category;

    document.getElementById("modalName").textContent=
        product.name;

    document.getElementById("modalBrand").textContent=
        "Brand: "+product.brand;

    document.getElementById("modalRating").innerHTML=
        "★★★★★ <span>"+
        product.rating+
        " • "+
        product.reviews.toLocaleString()+
        " customer reviews</span>";

    document.getElementById("modalDescription").textContent=
        product.description;

    document.getElementById("modalPrice").textContent=
        product.price.toLocaleString();

    document.getElementById("modalOldPrice").textContent=
        "₹"+product.oldPrice.toLocaleString();

    document.getElementById("modalStock").textContent=
        "✓ "+product.stock+" • "+product.delivery;

    document.getElementById("modalHighlights").innerHTML=
        product.highlights
        .map(item=>`<li>${item}</li>`)
        .join("");

    document.getElementById("modalSpecs").innerHTML=
        Object.entries(product.specs)
        .map(([key,value])=>`

            <div class="spec-row">

                <span>
                    ${key}
                </span>

                <span>
                    ${value}
                </span>

            </div>

        `)
        .join("");

    document.getElementById("modalSeller").innerHTML=
        "<strong>Seller</strong><br>"+
        product.seller;

    document.getElementById("modalCart").onclick=function(){

        addToCart(product.id);

        closeModal();
    };

    document.getElementById("productModal")
        .classList.add("show");

    document.body.classList.add("modal-open");
}

function closeModal(){

    document.getElementById("productModal")
        .classList.remove("show");

    if(!document.getElementById("cartPanel").classList.contains("open") &&
       !document.getElementById("imageModal").classList.contains("show")){

        document.body.classList.remove("modal-open");
    }
}

function toggleDark(){

    document.body.classList.toggle("dark");

    if(document.body.classList.contains("dark")){

        showToast("Dark mode enabled 🌙");

    }else{

        showToast("Light mode enabled ☀️");
    }
}

function checkout(){

    if(cart.length===0){

        showToast("Your cart is empty");

        return;
    }

    alert(
        "WebNova Checkout\n\n"+
        "Your order is ready for checkout.\n\n"+
        "Payment gateway integration can be added in the future version."
    );
}

function openImageSearch(){

    document.getElementById("imageModal")
        .classList.add("show");

    document.body.classList.add("modal-open");
}

function closeImageSearch(){

    document.getElementById("imageModal")
        .classList.remove("show");

    if(!document.getElementById("productModal").classList.contains("show") &&
       !document.getElementById("cartPanel").classList.contains("open")){

        document.body.classList.remove("modal-open");
    }
}

function previewImage(event){

    let file=event.target.files[0];

    let preview=
        document.getElementById("imagePreview");

    if(file){

        preview.src=
            URL.createObjectURL(file);

        preview.style.display="block";
    }
}

function imageSearchResult(){

    let file=
        document.getElementById("imageInput").files[0];

    if(!file){

        showToast(
            "Please select an image first"
        );

        return;
    }

    closeImageSearch();

    document.getElementById("shop")
        .scrollIntoView();

    showToast(
        "Visual search prototype activated 📷"
    );
}

function subscribe(){

    let email=
        document.getElementById("email")
        .value.trim();

    if(!email || !email.includes("@")){

        showToast(
            "Please enter a valid email"
        );

        return;
    }

    showToast(
        "Successfully subscribed ✨"
    );

    document.getElementById("email")
        .value="";
}

function showToast(message){

    let toast=
        document.getElementById("toast");

    toast.textContent=message;

    toast.classList.add("show");

    clearTimeout(window.toastTimer);

    window.toastTimer=setTimeout(()=>{

        toast.classList.remove("show");

    },2500);
}

let saleSeconds=
    8*60*60+
    30*60;

function updateCountdown(){

    let hours=
        Math.floor(saleSeconds/3600);

    let minutes=
        Math.floor(
            (saleSeconds%3600)/60
        );

    let seconds=
        saleSeconds%60;

    document.getElementById("hours").textContent=
        String(hours).padStart(2,"0");

    document.getElementById("minutes").textContent=
        String(minutes).padStart(2,"0");

    document.getElementById("seconds").textContent=
        String(seconds).padStart(2,"0");

    if(saleSeconds>0){

        saleSeconds--;

    }else{

        saleSeconds=
            8*60*60+
            30*60;
    }
}

setInterval(
    updateCountdown,
    1000
);

document.getElementById("productModal")
.addEventListener("click",function(event){

    if(event.target===this){

        closeModal();
    }
});

document.getElementById("imageModal")
.addEventListener("click",function(event){

    if(event.target===this){

        closeImageSearch();
    }
});

displayProducts();
updateCart();
updateCountdown();
</script>

</body>
</html>
