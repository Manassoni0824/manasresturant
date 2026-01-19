# manasresturant
for resturant 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Restaurant Menu - Offline Site</title>
    <style>
        /* Basic styling for a clean look */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #ff5722; /* Orange theme for restaurant feel */
            color: white;
            text-align: center;
            padding: 20px;
        }
        .menu {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        .item {
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            padding: 15px;
            text-align: center;
        }
        .item img {
            width: 100%;
            height: 150px;
            object-fit: cover;
            border-radius: 8px;
            margin-bottom: 10px;
        }
        .item h3 {
            margin: 0 0 10px 0;
            color: #ff5722;
        }
        .item p {
            margin: 5px 0;
        }
        .item button {
            background: #ff5722;
            color: white;
            border: none;
            padding: 8px 12px;
            border-radius: 4px;
            cursor: pointer;
            margin-top: 10px;
        }
        .item select {
            margin: 5px 0;
            padding: 5px;
        }
        .cart {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .cart h2 {
            text-align: center;
            color: #ff5722;
        }
        .cart-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }
        .cart-item button {
            background: #ccc;
            border: none;
            padding: 5px;
            cursor: pointer;
        }
        .order-details {
            margin: 10px 0;
        }
        .order-details label {
            display: block;
            margin: 5px 0;
        }
        .order-details input, .order-details select {
            padding: 5px;
            width: 100%;
            max-width: 200px;
        }
        .total {
            font-weight: bold;
            text-align: right;
            margin-top: 10px;
        }
        .place-order {
            background: #ff5722;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            display: block;
            margin: 10px auto;
        }
        .daily-stats {
            max-width: 1200px;
            margin: 20px auto;
            padding: 20px;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            text-align: center;
        }
        .daily-stats h2 {
            color: #ff5722;
        }
        .contact-section {
            padding: 20px;
            max-width: 600px;
            margin: 20px auto;
            background: white;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .contact-section h2 {
            text-align: center;
            color: #ff5722;
        }
        .contact-section form {
            display: flex;
            flex-direction: column;
        }
        .contact-section label {
            margin-top: 10px;
        }
        .contact-section input, .contact-section textarea {
            width: 100%;
            padding: 8px;
            margin: 5px 0;
            border: 1px solid #ccc;
            border-radius: 4px;
        }
        .contact-section button {
            background: #ff5722;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 4px;
            margin-top: 10px;
            cursor: pointer;
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #333;
            color: white;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Manas's resturant</h1>
        <p>Enjoy our delicious menu items!</p>
    </header>
<section class="menu">
    <div class="item">
        <img src="images/noodles.jpg" alt="Delicious stir-fried noodles">
        <h3>Noodles</h3>
        <p>Delicious stir-fried noodles with veggies and sauce.</p>
        <p><strong>Price:</strong> $70</p>
        <button onclick="addToCart('Noodles', 70)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/pasta.jpg" alt="Creamy pasta dish">
        <h3>Pasta</h3>
        <p>Creamy pasta with your choice of toppings.</p>
        <p><strong>Price:</strong> $60</p>
        <button onclick="addToCart('Pasta', 60)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/pizza.jpg" alt="Wood-fired pizza">
        <h3>Pizza</h3>
        <p>Wood-fired pizza with fresh ingredients.</p>
        <p><strong>Price:</strong> $ 50 to 280</p>
        <button onclick="addToCart('Pizza', 50)">Add to Cart</button> <!-- Assumed base $50; adjust as needed -->
    </div>
    <div class="item">
        <img src="images/shisha.jpg" alt="Relaxing shisha setup">
        <h3>Shisha</h3>
        <p>Relaxing shisha flavors for a unique experience.</p>
        <p><strong>Price:</strong> $ 350 </p>
        <button onclick="addToCart('Shisha', 350)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/momos.jpg" alt="Steamed dumplings">
        <h3>Momos</h3>
        <p>Steamed dumplings filled with spiced meat or veggies.</p>
        <p><strong>Price:</strong> $50</p>
        <button onclick="addToCart('Momos', 50)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/colddrinks.jpg" alt="Refreshing cold drinks">
        <h3>Cold Drinks</h3>
        <p>Refreshing sodas and juices to cool you down.</p>
        <p><strong>Price:</strong> $20</p>
        <button onclick="addToCart('Cold Drinks', 20)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/friedrice.jpg" alt="Flavorful fried rice">
        <h3>Fried Rice</h3>
        <p>Flavorful fried rice with eggs and mixed veggies.</p>
        <p><strong>Price:</strong> $ 80</p>
        <button onclick="addToCart('Fried Rice', 80)">Add to Cart</button>
    </div>
    <div class="item">
        <img src="images/manchuriyan.jpg" alt="Crispy vegetable balls in sauce">
        <h3>Manchuriyan</h3>
        <p>Crispy vegetable balls in tangy sauce.</p>
        <p><strong>Price:</strong> Half- 50, Full- 80</p>
        <select id="manchuriyan-size">
            <option value="50">Half ($50)</option>
            <option value="80">Full ($80)</option>
        </select>
        <button onclick="addManchuriyan()">Add to Cart</button>
    </div>
</section>
<section class="cart">
    <h2>Your Cart</h2>
    <div id="cart-items"></div>
    <div class="order-details">
        <label for="order-date">Order Date:</label>
        <input type="date" id="order-date">
        <label for="table-number">Table Number (0-10):</label>
        <select id="table-number">
            <option value="0">0 (Takeaway/No Table)</option>
            <option value="1">1</option>
            <option value="2">2</option>
            <option value="3">3</option>
            <option value="4">4</option>
            <option value="5">5</option>
            <option value="6">6</option>
            <option value="7">7</option>
            <option value="8">8</option>
            <option value="9">9</option>
            <option value="10">10</option>
        </select>
    </div>
    <div class="total">Total: $<span id="total-price">0</span></div>
    <button class="place-order" onclick="placeOrder()">Place Order</button>
</section>
<section class="daily-stats">
    <h2>Daily Stats</h2>
    <p>Orders Today: <span id="daily-orders">0</span></p>
    <p>Money Collected Today: $<span id="daily-collection">0</span></p>
</section>
<section class="contact-section">
    <h2>Contact Us</h2>
    <form>
        <label for="name">Name:</label><br>
        <input type="text" id="name" name="name"><br>
        <label for="email">Email:</label><br>
        <input type="email" id="email" name="email"><br>
        <label for="message">Message:</label><br>
        <textarea id="message" name="message"></textarea><br>
        <button type="submit">Send</button>
    </form>
</section>
<footer>
    <p>&copy; 2026 Restaurant Name. All rights reserved. | Contact: 7309678900 , Manas's01@restaurant.com</p>
</footer>
<script>
    let cart = [];
    let total = 0;

    // Load daily stats from localStorage
    let today = new Date().toDateString();
    let dailyStats = JSON.parse(localStorage.getItem('dailyStats')) || { date: today, orders: 0, collection: 0 };
    if (dailyStats.date !== today) {
        dailyStats = { date: today, orders: 0, collection: 0 };
    }
    updateDailyStatsDisplay();

    function addToCart(itemName, price) {
        const existingItem = cart.find(item => item.name === itemName);
        if (existingItem) {
            existingItem.quantity++;
        } else {
            cart.push({ name: itemName, price: price, quantity: 1 });
        }
        updateCart();
    }

    function addManchuriyan() {
        const sizeSelect = document.getElementById('manchuriyan-size');
        const price = parseInt(sizeSelect.value);
        const size = sizeSelect.options[sizeSelect.selectedIndex].text;
        const itemName = `Manchuriyan (${size})`;
        addToCart(itemName, price);
    }

    function updateCart() {
        const cartItemsDiv = document.getElementById('cart-items');
        cartItemsDiv.innerHTML = '';
        total = 0;
        cart.forEach((item, index) => {
            total += item.price * item.quantity;
            cartItemsDiv.innerHTML += `
                <div class="cart-item">
                    <span>${item.name} (x${item.quantity}) - $${item.price * item.quantity}</span>
                    <div>
                        <button onclick="changeQuantity(${index}, 1)">+</button>
                        <button onclick="changeQuantity(${index}, -1)">-</button>
                        <button onclick="removeItem(${index})">Remove</button>
                    </div>
                </div>
            `;
        });
        document.getElementById('total-price').textContent = total;
    }

    function changeQuantity(index, change) {
        cart[index].quantity += change;
        if (cart[index].quantity <= 0) {
            cart.splice(index, 1);
        }
        updateCart();
    }

    function removeItem(index) {
        cart.splice(index, 1);
        updateCart();
    }

    function placeOrder() {
        if (cart.length === 0) {
            alert('Your cart is empty!');
            return;
        }
        const orderDate = document.getElementById('order-date').value || new Date().toISOString().split('T')[0];
        const tableNumber = document.getElementById('table-number').value;
        let orderSummary = `Order Summary:\nDate: ${orderDate}\nTable Number: ${tableNumber}\n\nItems:\n`;
        cart.forEach(item => {
            orderSummary += `${item.name} (x${item.quantity}) - $${item.price * item.quantity}\n`;
        });
        orderSummary += `\nTotal: $${total}\n\nThank you for your order! (This is offline - contact us at 7309678900 for real orders.)`;
        alert(orderSummary);

        // Update daily stats
        dailyStats.orders++;
        dailyStats.collection += total;
        localStorage.setItem('dailyStats', JSON.stringify(dailyStats));
        updateDailyStatsDisplay();

        cart = [];
        updateCart();
    }

    function updateDailyStatsDisplay() {
        document.getElementById('daily-orders').textContent = dailyStats.orders;
        document.getElementById('daily-collection').textContent = dailyStats.collection;
    }
</script>
</body>
</html> 
