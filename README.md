
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>More Gaming - Sale!</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Header met taalkeuze, zoekbalk, en feedback/inloggen knop -->
    <header>
        <div class="header-content">
            <div class="language-selector">
                <select id="language" onchange="changeLanguage()">
                    <option value="en">English</option>
                    <option value="nl">Nederlands</option>
                </select>
            </div>

            <!-- Zoekbalk bovenaan de pagina -->
            <div class="search-container">
                <form action="search.html" method="get" class="search-form">
                    <input type="text" name="search" placeholder="Search for products..." class="search-input">
                    <button type="submit" class="search-button">Search</button>
                </form>
            </div>
        </div>
    </header>

    <main>
        <!-- Populaire Producten Sectie -->
        <section class="product-section">
            <h2>Our Popular Products</h2>
            <div class="product-list">
                <div class="product">
                    <img src="images/fortnite-headset.jpg" alt="Fortnite Gaming Headset">
                    <p>Fortnite Gaming Headset</p>
                    <p>€15,59</p>
                    <p>Bezorgdatum: <span class="delivery-date"></span></p>
                </div>

                <div class="product">
                    <img src="images/logitech-gaming-mouse.jpg" alt="Logitech Gaming Mouse">
                    <p>Logitech Gaming Mouse</p>
                    <p>€19,99</p>
                    <p>Bezorgdatum: <span class="delivery-date"></span></p>
                </div>

                <div class="product">
                    <img src="images/razer-gaming-keyboard.jpg" alt="Razer Gaming Keyboard">
                    <p>Razer Gaming Keyboard</p>
                    <p>€89,99</p>
                    <p>Bezorgdatum: <span class="delivery-date"></span></p>
                </div>

                <div class="product">
                    <img src="images/fortnite-phone-case.jpg" alt="Fortnite Phone Case">
                    <p>Fortnite Phone Case</p>
                    <p>€9,99</p>
                    <p>Bezorgdatum: <span class="delivery-date"></span></p>
                </div>
            </div>
        </section>

        <!-- Sale! Sectie met timer en producten -->
        <section class="sale-section">
            <h2>Sale! <span id="countdown"></span></h2>
            <div class="product-list" id="sale-products">
                <!-- Dynamische producten komen hier -->
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2025 More Gaming. All rights reserved.</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
<!-- Sale Sectie -->
<section class="sale-section">
    <h2>Sale! Limited Time Offer</h2>
    <div id="countdown"></div> <!-- Countdown timer -->
    <div id="sale-products">
        <!-- Dynamisch geladen sale-producten komen hier -->
    </div>
</section>

<!-- Populaire Producten Sectie -->
<section class="product-section">
    <h2>Our Popular Products</h2>
    <div class="product-list">
        <!-- Product 1 -->
        <div class="product">
            <img src="gaming-headset.jpg" alt="Fortnite Gaming Headset">
            <p>Fortnite Gaming Headset</p>
            <p>€15,59</p>
            <p>Bezorgdatum: <span class="delivery-date"></span></p>
        </div>

        <!-- Product 2 -->
        <div class="product">
            <img src="gaming-mouse.jpg" alt="Fortnite Gaming Mouse">
            <p>Logitech gaming Mouse</p>
            <p>€19,99</p>
            <p>Bezorgdatum: <span class="delivery-date"></span></p>
        </div>

        <!-- Product 3 -->
        <div class="product">
            <img src="gaming-keyboard.jpg" alt="Fortnite Gaming Keyboard">
            <p>Fortnite Gaming Keyboard</p>
            <p>€89,99</p>
            <p>Bezorgdatum: <span class="delivery-date"></span></p>
        </div>

        <!-- Product 4 -->
        <div class="product">
            <img src="fortnite-phone-case.jpg" alt="Fortnite Phone Case">
            <p>Fortnite Phone Case</p>
            <p>€9,99</p>
            <p>Bezorgdatum: <span class="delivery-date"></span></p>
        </div>
    </div>
</section>
/* Algemene opmaak voor de header */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: #333;
    color: white;
}

/* Zorg dat de zoekbalk volledig gecentreerd is bovenaan */
.header-content {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
}

.search-container {
    flex-grow: 1;
    display: flex;
    justify-content: center;
    align-items: center;
}

.search-form {
    display: flex;
    justify-content: center;
    width: 100%;
}

.search-input {
    padding: 8px;
    font-size: 16px;
    width: 300px;
    text-align: center;
}

.search-button {
    padding: 8px 15px;
    font-size: 16px;
    background-color: #444;
    color: white;
    border: none;
    cursor: pointer;
}

.search-button:hover {
    background-color: #555;
}

/* Sale sectie */
.sale-section {
    background-color: #f9f9f9;
    padding: 20px;
    margin-top: 50px;
    text-align: center;
}

.sale-section h2 {
    font-size: 2rem;
    color: #e74c3c;
}

#countdown {
    font-size: 1.5rem;
    color: #ff6347; /* Roze-oranje kleur voor de timer */
    font-weight: bold;
    margin-left: 10px;
}

/* Producten in sale */
.sale-product {
    width: 200px;
    text-align: center;
    background-color: #f8f8f8;
    padding: 15px;
    border-radius: 5px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
    margin: 10px;
}

.sale-product img {
    width: 100%;
    height: auto;
    border-radius: 5px;
}

.sale-product .old-price {
    text-decoration: line-through;
    color: gray;
}

.sale-product .new-price {
    color: #e74c3c;
    font-size: 1.2rem;
}

/* Producten sectie styling */
.product-list {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
}

.product {
    width: 200px;
    text-align: center;
    background-color: #f8f8f8;
    padding: 15px;
    border-radius: 5px;
    box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
}

.product img {
    width: 100%;
    height: auto;
    border-radius: 5px;
}

.product p {
    margin: 10px 0;
}

/* Footer styling */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px;
}
       
