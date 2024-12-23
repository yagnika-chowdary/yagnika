!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delightful Bites Restaurant</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Custom Animations */
        .fade-in {
            animation: fadeIn 1.5s ease-in-out;
        }

        .slide-up {
            animation: slideUp 1s ease-out;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }

        @keyframes slideUp {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">
    <!-- Navigation -->
    <nav class="bg-white shadow-lg sticky top-0 z-50">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center fade-in">
            <a href="#" class="text-2xl font-bold text-green-600 hover:text-green-800">Delightful Bites</a>
            <div class="space-x-6">
                <a href="#menu" class="text-gray-800 hover:text-green-600 transition duration-300">Menu</a>
                <a href="#about" class="text-gray-800 hover:text-green-600 transition duration-300">About</a>
                <a href="#gallery" class="text-gray-800 hover:text-green-600 transition duration-300">Gallery</a>
                <a href="#contact" class="text-gray-800 hover:text-green-600 transition duration-300">Contact</a>
                <button id="cart-btn" class="bg-green-500 text-white px-4 py-2 rounded-lg shadow hover:bg-green-600 transition duration-300">
                    Cart (<span id="cart-count">0</span>)
                </button>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="bg-cover bg-center h-[600px] relative" style="background-image: url('https://source.unsplash.com/1200x800/?restaurant');">
        <div class="absolute inset-0 bg-black bg-opacity-50 flex items-center justify-center">
            <div class="text-center text-white p-8 rounded-lg slide-up">
                <h1 class="text-5xl font-extrabold mb-4">Welcome to Delightful Bites</h1>
                <p class="text-2xl">Exquisite Cuisine, Unforgettable Experience</p>
                <a href="#menu" class="inline-block mt-6 bg-green-500 text-white px-6 py-3 rounded-lg shadow hover:bg-green-600 transition duration-300">
                    Explore Menu
                </a>
            </div>
        </div>
    </header>

    <!-- Menu Section -->
    <section id="menu" class="container mx-auto my-16 px-6">
        <h2 class="text-4xl font-bold text-center mb-10 fade-in">Our Menu</h2>
        <div id="menu-items" class="grid md:grid-cols-3 gap-8">
            <!-- Menu items will be dynamically added here -->
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="container mx-auto my-16 px-6">
        <h2 class="text-4xl font-bold text-center mb-10 fade-in">About Us</h2>
        <p class="text-lg text-gray-700 text-center max-w-3xl mx-auto fade-in">
            At Delightful Bites, we are dedicated to providing exceptional culinary experiences that delight your taste buds and leave a lasting impression. Our team of experienced chefs uses the freshest ingredients to create dishes that are as delicious as they are memorable. Join us for a dining experience like no other!
        </p>
    </section>

    <!-- Gallery Section -->
    <section id="gallery" class="container mx-auto my-16 px-6">
        <h2 class="text-4xl font-bold text-center mb-10 fade-in">Gallery</h2>
        <div class="grid md:grid-cols-3 gap-6 fade-in">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRrALs2gUhSyftPQPc_B5evmTp57gVEoGaouw&s" alt="Restaurant Interior" class="rounded-lg shadow-md">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSHzIu1xsyWd4cBCkwvqdEQQgwfb3rrYC28vQ&s" alt="Dining Table" class="rounded-lg shadow-md">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT4tXj_PGb1vPThrUndOWdRGR_EQieIlUwZtA&s" alt="Chef at Work" class="rounded-lg shadow-md">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRMFIqm-v9UtnUnOrPFFEc2Z7izl1OtdP-mvg&s" alt="Beautiful Lighting" class="rounded-lg shadow-md">
            <img src="https://t3.ftcdn.net/jpg/02/60/12/88/360_F_260128861_Q2ttKHoVw2VrmvItxyCVBnEyM1852MoJ.jpg" alt="Delicious Food" class="rounded-lg shadow-md">
            <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTDbsMYPhDbzF8k8TVVha_81HCmapOwFtymDw&s" alt="Modern Kitchen" class="rounded-lg shadow-md">
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="container mx-auto my-16 px-6">
        <h2 class="text-4xl font-bold text-center mb-10 fade-in">Contact Us</h2>
        <form class="max-w-lg mx-auto space-y-6 fade-in">
            <div>
                <label for="name" class="block text-gray-700 font-bold mb-2">Name:</label>
                <input type="text" id="name" class="w-full p-3 border rounded focus:outline-none focus:ring-2 focus:ring-green-500" placeholder="Your Name" required>
            </div>
            <div>
                <label for="email" class="block text-gray-700 font-bold mb-2">Email:</label>
                <input type="email" id="email" class="w-full p-3 border rounded focus:outline-none focus:ring-2 focus:ring-green-500" placeholder="Your Email" required>
            </div>
            <div>
                <label for="message" class="block text-gray-700 font-bold mb-2">Message:</label>
                <textarea id="message" class="w-full p-3 border rounded h-32 focus:outline-none focus:ring-2 focus:ring-green-500" placeholder="Your Message" required></textarea>
            </div>
            <button type="submit" class="w-full bg-green-500 text-white py-3 rounded-lg shadow hover:bg-green-600 transition duration-300">
                Send Message
            </button>
        </form>
    </section>

    <!-- Location Section -->
    <section id="location" class="container mx-auto my-16 px-6">
        <h2 class="text-4xl font-bold text-center mb-10 fade-in">Our Location</h2>
        <div id="map" class="w-full h-96 fade-in">
            <iframe 
                src="https://www.openstreetmap.org/export/embed.html?bbox=-73.947582%2C40.719438%2C-73.922874%2C40.741629&layer=mapnik&marker=40.730534%2C-73.935228" 
                style="border:0; width: 100%; height: 100%;" 
                allowfullscreen="" 
                loading="lazy">
            </iframe>
        </div>
    </section>

    <!-- Cart Modal -->
    <div id="cart-modal" class="fixed inset-0 bg-black bg-opacity-50 hidden z-50 flex items-center justify-center">
        <div class="bg-white rounded-lg p-8 max-w-lg w-full transform scale-95 transition-transform duration-300">
            <div class="flex justify-between items-center mb-4">
                <h2 class="text-2xl font-bold">Your Cart</h2>
                <button id="close-cart" class="text-red-500 hover:text-red-700">Close</button>
            </div>
            <div id="cart-items" class="space-y-4 mb-4">
                <!-- Cart items will be dynamically added here -->
            </div>
            <div class="border-t pt-4">
                <div class="flex justify-between mb-4">
                    <span class="font-bold">Total:</span>
                    <span id="cart-total">$0.00</span>
                </div>
                <button id="checkout-btn" class="w-full bg-green-500 text-white py-3 rounded-lg shadow hover:bg-green-600 transition duration-300">
                    Proceed to Checkout
                </button>
            </div>
        </div>
    </div>

    <script>
        // Menu Items Data
        const menuItems = [
            { id: 1, name: 'Margherita Pizza', price: 12.99, image: 'https://ca.ooni.com/cdn/shop/articles/20220211142645-margherita-9920.jpg?crop=center&height=915&v=1661341987&width=1200' },
            { id: 2, name: 'Caesar Salad', price: 8.50, image: 'https://cdn.loveandlemons.com/wp-content/uploads/2024/12/caesar-salad.jpg' },
            { id: 3, name: 'Grilled Salmon', price: 18.99, image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRnC2p7osU5rqS-9mXW8IVtilKYpAMKQPWdxw&s' },
            { id: 4, name: 'Vegetarian Pasta', price: 14.50, image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRKJHMs4My3OUj4hgaGObfXZI1bUasnd5oUhg&s' },
            { id: 5, name: 'Chicken Burger', price: 11.99, image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQqVL56hNet6FNNKXkL6KaPyUZ7iz1ePMsh5g&s' },
            { id: 6, name: 'Chocolate Brownie', price: 6.99, image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQUgLs3F7VS7IYwO8D3-lI2hC76Lzic792YUg&s' }
        ];

        // Cart Management
        let cart = [];

        function renderMenuItems() {
            const menuContainer = document.getElementById('menu-items');
            menuContainer.innerHTML = menuItems.map(item => `
                <div class="bg-white rounded-lg shadow-md overflow-hidden hover:shadow-lg transition duration-300">
                    <img src="${item.image}" alt="${item.name}" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <h3 class="font-bold text-lg mb-2">${item.name}</h3>
                        <div class="flex justify-between items-center">
                            <span class="text-green-600 font-bold">$${item.price.toFixed(2)}</span>
                            <button onclick="addToCart(${item.id})" class="bg-green-500 text-white px-3 py-1 rounded-lg hover:bg-green-600 transition duration-300">
                                Add to Cart
                            </button>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        function addToCart(itemId) {
            const item = menuItems.find(i => i.id === itemId);
            const existingItem = cart.find(i => i.id === itemId);

            if (existingItem) {
                existingItem.quantity++;
            } else {
                cart.push({ ...item, quantity: 1 });
            }

            updateCart();
        }

        function updateCart() {
            const cartCount = document.getElementById('cart-count');
            const cartItems = document.getElementById('cart-items');
            const cartTotal = document.getElementById('cart-total');

            const totalItems = cart.reduce((sum, item) => sum + item.quantity, 0);
            const total = cart.reduce((sum, item) => sum + item.price * item.quantity, 0);

            cartCount.textContent = totalItems;
            cartItems.innerHTML = cart.map(item => `
                <div class="flex justify-between items-center">
                    <span>${item.name} x ${item.quantity}</span>
                    <span>$${(item.price * item.quantity).toFixed(2)}</span>
                </div>
            `).join('');

            cartTotal.textContent = `$${total.toFixed(2)}`;
        }

        // Cart Modal Functionality
        document.getElementById('cart-btn').addEventListener('click', () => {
            const modal = document.getElementById('cart-modal');
            modal.classList.remove('hidden');
            modal.querySelector('div').classList.remove('scale-95');
        });

        document.getElementById('close-cart').addEventListener('click', () => {
            const modal = document.getElementById('cart-modal');
            modal.classList.add('hidden');
            modal.querySelector('div').classList.add('scale-95');
        });

        document.getElementById('checkout-btn').addEventListener('click', () => {
            alert('Thanks for ordering! Your order is being processed.');
            document.getElementById('cart-modal').classList.add('hidden');
        });

        // Initialize Menu
        renderMenuItems();
    </script>
</body>
</html> <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Pizza Landing Page</title>
    <!-- Box Icons -->
    <link rel="stylesheet"
  href="https://unpkg.com/boxicons@latest/css/boxicons.min.css">
  <!-- Link To CSS -->
  <link rel="stylesheet" href="code.css">

</head>
<body>
    <!-- Navbar -->
    <header>
        <a href="#" class="logo">Pizza Pie</a>
        <div class="bx bx-menu" id="menu-icon"></div>

        <ul class="navbar">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#menu">Menu</a></li>
            <li><a href="#services">Service</a></li>
            <li><a href="#contact">Contact</a></li>
            <!-- Dark Mode -->
            <div class="bx bx-moon" id="darkmode"></div>
        </ul>
    </header>
    <!-- Home Section-->
    <section class="home" id="home">
        <div class="home-text">
            <h1>Pizza Taste</h1>
            <h2>The tasty pizza of <br> your choice</h2>
            <a href="file:///C:/Users/LENOVO/Desktop/script.html">View Menu</a>
        </div>
        <div class="home-img">
            <img src= "C:\Users\LENOVO\Desktop\pizza.jpg" alt="pizzi">
        </div>
    </section>

    <!-- About -->
    <section class="about" id="about">
        <div class="about-img">
            <img src=C:\Users\LENOVO\Desktop\pizzi2.jpg alt="">
        </div>
        <div class="about-text">
            <span>About Us</span>
            <h2>We make good and <br> tasty pizzas</h2>
            <p>Whether you're hosting a party or indulging in a solo feast, we ensure quick delivery straight to your doorstep.</p>
            <a href="file:///C:/Users/LENOVO/Desktop/index.html">Learn More</a>
        </div>
    </section>

    <!-- Menu -->
    <section class="menu" id="menu">

        <div class="heading">
            <span>Menu</span>
            <h2>Tasty menu of the week</h2>
        </div>
        <div class="menu-container">
            <!-- Box 1 -->
            <div class="box">
                <div class="box-img">
                    <img src="https://images.pexels.com/photos/803290/pexels-photo-803290.jpeg?cs=srgb&dl=pexels-beqa-tefnadze-803290.jpg&fm=jpg" alt="">
                </div>
                <h2>Cheese Pizza</h2>
                <h3>Tasty Food</h3>
                <span>$30.05</span>
                <i class='bx bx-cart-alt'></i>
            </div>
            <!-- Box 2 -->
            <div class="box">
                <div class="box-img">
                    <img src="https://img.freepik.com/free-photo/pepperoni-pizza-with-sausages-cheese-dark-wooden-table_220768-9277.jpg?size=626&ext=jpg" alt="">
                </div>
                <h2>Tropical Pizza</h2>
                <h3>Tasty Food</h3>
                <span>$42.05</span>
                <i class='bx bx-cart-alt'></i>
            </div>
            <!-- Box 3 -->
            <div class="box">
                <div class="box-img">
                    <img src="https://img.freepik.com/free-photo/top-view-pepperoni-pizza-with-mushroom-sausages-bell-pepper-olive-corn-black-wooden_141793-2158.jpg?w=740&t=st=1661842808~exp=1661843408~hmac=c40f0c154036b96b1dba17947c4e4f7c07f40db983106490402bb0b7b6ec452e" alt="">
                </div>
                <h2>Mecaroni Pizza</h2>
                <h3>Tasty Food</h3>
                <span>$12.05</span>
                <i class='bx bx-cart-alt'></i>
            </div>
        </div>
    </section>

    <!-- Service -->
    <section class="services" id="services">
        <div class="heading">
            <span>Services</span>
            <h2>We provide best food services</h2>
        </div>

        <div class="servives-container">
            <!-- Box 1 -->
            <div class="s-box">
                <img src="https://images.pexels.com/photos/280453/pexels-photo-280453.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500.png" alt="">
                <h3>You Order</h3>
                <p>Order Your Favorite Pizza 🍕
Craving delicious, hot, and cheesy pizza? You’re just a few clicks away from satisfying your taste buds!

.</p>
            </div>
            <!-- Box 2 -->
            <div class="s-box">
                <img src="https://images.pexels.com/photos/4391470/pexels-photo-4391470.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500.png" alt="">
                <h3>Shipping</h3>
                <p>Fast Delivery: Piping hot pizza delivered right to your doorstep!
Satisfaction Guaranteed: We promise you'll love every bite..</p>
            </div>
            <!-- Box 3 -->
            <div class="s-box">
                <img src="https://images.pexels.com/photos/4393426/pexels-photo-4393426.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500.png" alt="">
                <h3>Delivered</h3>
                <p>Special Offers on Delivery
Free Delivery: On orders above $20.
Combo Deals: Add sides and drinks to your order and save big!
Loyalty Rewards: Earn points every time you order and redeem them for discounts.
</p>
            </div>
        </div>
    </section>

    <!-- Connect -->
    <section class="connect">
        <div class="connect-text">
            <span>Let's Talk</span>
            <h2>Connect now</h2>
        </div>
        <a href="file:///C:/Users/LENOVO/Desktop/contact.html">Contact Us</a>
    </section>

    <!-- Contact -->
    <section class="contact" id="contact">
        <div class="contact-box">
            <h3>Pizza Pie</h3>
            <span>Connect With Us</span>
            <div class="social">
                <a href="#"><i class='bx bxl-facebook' ></i></a>
                <a href="#"><i class='bx bxl-twitter' ></i></a>
                <a href="#"><i class='bx bxl-instagram' ></i></a>
            </div>
        </div>
        <div class="contact-box">
            <h3>Menu Links</h3>
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#menu">Menu</a></li>
            <li><a href="#services">Service</a></li>
            <li><a href="#contact">Contact</a></li>
        </div>
        <div class="contact-box">
            <h3>Quick Links</h3>
            <li><a href="#Contact">Contact</a></li>
            <li><a href="#Privacy Policy">Privacy Policy</a></li>
            <li><a href="#Disclaimer">Disclaimer</a></li>
            <li><a href="#Terms Of Use">Terms Of Use</a></li>
        </div>
        <div class="contact-box address">
            <h3>Contact</h3>
            <i class='bx bxs-map' ><span>005,Dayananda Sagar University,Harohalli,Karnataka,562112,India</span></i>
<a href="https://www.dsu.edu.in/">Dayananda Sagar university</a>
            <i class='bx bxs-phone' ><span>+91 698 9345 783</span></i>
            <i class='bx bxs-envelope' ><span>pizzeriaatmyuni@email.com</span></i>
        </div>
    </section>

    <!-- Copyright -->
    <div class="copyright">
        <p>©️ Asslone4 All Right Reserved.</p>
    </div>


    <!-- Scroll Reveal -->
    <script src="https://unpkg.com/scrollreveal"></script>
    <!-- Link To JavaScript -->
    <script src="code.js"></script>
</body>
</html> /* Google Fonts */
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
  * {
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    box-sizing: border-box;
    scroll-behavior: smooth;
    scroll-padding-top: 2rem;
    list-style: none;
    text-decoration: none;
  }
  *::selection {
    background: var(--main-color);
    color: #fff;
  }
  :root {
    --main-color: #ffb411;
    --text-c

          <i class='bx bxs-map' ><span>005,Dayananda Sagar University,Harohalli,Karnataka,562112,India</span></i>
<a href="https://www.dsu.edu.in/">Dayananda Sagar university</a>
            <i class='bx bxs-phone' ><span>+91 698 9345 783</span></i>
            <i class='bx bxs-envelope' ><span>pizzeriaatmyuni@email.com</span></i>
        </div>
    </section>

    <!-- Copyright -->
    <div class="copyright">
        <p>©️ Asslone4 All Right Reserved.</p>
    </div>


    <!-- Scroll Reveal -->
    <script src="https://unpkg.com/scrollreveal"></script>
    <!-- Link To JavaScript -->
    <script src="code.js"></script>
</body>
</html> /* Google Fonts */
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
  * {
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    box-sizing: border-box;
    scroll-behavior: smooth;
    scroll-padding-top: 2rem;
    list-style: none;
    text-decoration: none;
  }
  *::selection {
    background: var(--main-color);
    color: #fff;
  }
  :root {
    --main-color: #ffb411;
    --text-c
          <i class='bx bxs-map' ><span>005,Dayananda Sagar University,Harohalli,Karnataka,562112,India</span></i>
<a href="https://www.dsu.edu.in/">Dayananda Sagar university</a>
            <i class='bx bxs-phone' ><span>+91 698 9345 783</span></i>
            <i class='bx bxs-envelope' ><span>pizzeriaatmyuni@email.com</span></i>
        </div>
    </section>

    <!-- Copyright -->
    <div class="copyright">
        <p>©️ Asslone4 All Right Reserved.</p>
    </div>


    <!-- Scroll Reveal -->
    <script src="https://unpkg.com/scrollreveal"></script>
    <!-- Link To JavaScript -->
    <script src="code.js"></script>
</body>
</html> /* Google Fonts */
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap");
  * {
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
    box-sizing: border-box;
    scroll-behavior: smooth;
    scroll-padding-top: 2rem;
    list-style: none;
    text-decoration: none;
  }
  *::selection {
    background: var(--main-color);
    color: #fff;
  }
  :root {
    --main-color: #ffb411;
    --text-c
