[index.html](https://github.com/user-attachments/files/25696706/index.html)
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MIPYME Aportando al Futuro - Bloques y Losas de Hormigón</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2c3e50;
            --secondary: #e67e22;
            --accent: #f39c12;
            --light: #ecf0f1;
            --dark: #1a252f;
            --success: #27ae60;
            --map-blue: #4285F4;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            overflow-x: hidden;
        }

        /* Header & Navigation */
        header {
            background: linear-gradient(135deg, var(--primary) 0%, var(--dark) 100%);
            color: white;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.3);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .logo i {
            color: var(--secondary);
            font-size: 2rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .cart-icon {
            position: relative;
            cursor: pointer;
            font-size: 1.5rem;
        }

        .cart-count {
            position: absolute;
            top: -10px;
            right: -10px;
            background: var(--secondary);
            color: white;
            border-radius: 50%;
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8rem;
            font-weight: bold;
        }

        /* Hero Section */
        .hero {
            margin-top: 80px;
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), url(bloques\ 151.jpg);
            background-size: cover;
            background-position: center;
            height: 80vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
            animation: fadeInUp 1s ease;
        }

        .hero-content p {
            font-size: 1.5rem;
            margin-bottom: 2rem;
            animation: fadeInUp 1s ease 0.3s both;
        }

        .cta-button {
            display: inline-block;
            padding: 1rem 2.5rem;
            background: var(--secondary);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: bold;
            transition: all 0.3s;
            animation: fadeInUp 1s ease 0.6s both;
            border: 2px solid var(--secondary);
        }

        .cta-button:hover {
            background: transparent;
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.3);
        }

        /* Stats Section */
        .stats {
            background: var(--primary);
            color: white;
            padding: 3rem 0;
        }

        .stats-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            padding: 0 2rem;
            text-align: center;
        }

        .stat-item {
            padding: 1rem;
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            color: var(--secondary);
            display: block;
        }

        .stat-label {
            font-size: 1.1rem;
            opacity: 0.9;
        }

        /* Products Section */
        .products {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 3rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 80px;
            height: 4px;
            background: var(--secondary);
            margin: 1rem auto;
            border-radius: 2px;
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .product-card {
            background: white;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.2);
        }

        .product-badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background: var(--secondary);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 25px;
            font-weight: bold;
            font-size: 0.9rem;
            z-index: 10;
        }

        .product-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .product-card:hover .product-image {
            transform: scale(1.05);
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-title {
            font-size: 1.5rem;
            color: var(--primary);
            margin-bottom: 0.5rem;
        }

        .product-specs {
            color: #666;
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }

        .product-price {
            font-size: 2rem;
            color: var(--secondary);
            font-weight: bold;
            margin-bottom: 1rem;
        }

        .product-price span {
            font-size: 1rem;
            color: #666;
        }

        .add-to-cart {
            width: 100%;
            padding: 1rem;
            background: var(--success);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
        }

        .add-to-cart:hover {
            background: #229954;
            transform: scale(1.02);
        }

        .quantity-selector {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 1rem;
        }

        .qty-btn {
            width: 30px;
            height: 30px;
            border: 1px solid #ddd;
            background: white;
            cursor: pointer;
            border-radius: 5px;
            font-weight: bold;
        }

        .qty-input {
            width: 60px;
            text-align: center;
            border: 1px solid #ddd;
            padding: 0.3rem;
            border-radius: 5px;
        }

        /* About Section */
        .about {
            padding: 5rem 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }

        .about-text p {
            margin-bottom: 1rem;
            color: #555;
            line-height: 1.8;
        }

        .about-image {
            position: relative;
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
        }

        .about-image img {
            width: 100%;
            height: auto;
            display: block;
        }

        /* Location & Contact Section */
        .location-section {
            background: linear-gradient(135deg, #f5f7fa 0%, #c3cfe2 100%);
            padding: 5rem 2rem;
        }

        .location-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .location-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            margin-top: 3rem;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 15px 35px rgba(0,0,0,0.1);
        }

        .map-container {
            position: relative;
            min-height: 500px;
        }

        .map-container iframe {
            width: 100%;
            height: 100%;
            min-height: 500px;
            border: none;
        }

        .location-info {
            padding: 3rem;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        .location-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }

        .location-icon {
            width: 60px;
            height: 60px;
            background: var(--map-blue);
            color: white;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8rem;
        }

        .location-title h3 {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 0.3rem;
        }

        .location-title p {
            color: #666;
        }

        .address-details {
            background: #f8f9fa;
            padding: 1.5rem;
            border-radius: 12px;
            margin-bottom: 2rem;
            border-left: 4px solid var(--map-blue);
        }

        .address-details h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .address-details p {
            color: #555;
            line-height: 1.6;
            margin-left: 1.5rem;
        }

        .map-buttons {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        .map-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0.8rem;
            padding: 1rem 1.5rem;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: 2px solid transparent;
        }

        .btn-primary-map {
            background: var(--map-blue);
            color: white;
        }

        .btn-primary-map:hover {
            background: #3367d6;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(66, 133, 244, 0.4);
        }

        .btn-secondary-map {
            background: white;
            color: var(--primary);
            border-color: #ddd;
        }

        .btn-secondary-map:hover {
            border-color: var(--map-blue);
            color: var(--map-blue);
            transform: translateY(-2px);
        }

        .hours-badge {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            background: #e8f5e9;
            color: #2e7d32;
            padding: 0.5rem 1rem;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            margin-top: 1rem;
        }

        /* Contact Section */
        .contact {
            background: var(--primary);
            color: white;
            padding: 5rem 2rem;
        }

        .contact-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-top: 3rem;
        }

        .contact-card {
            background: rgba(255,255,255,0.1);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            backdrop-filter: blur(10px);
            transition: transform 0.3s;
        }

        .contact-card:hover {
            transform: translateY(-5px);
            background: rgba(255,255,255,0.15);
        }

        .contact-icon {
            font-size: 3rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }

        .contact-card h3 {
            margin-bottom: 0.5rem;
            font-size: 1.3rem;
        }

        .contact-card p {
            opacity: 0.9;
        }

        .contact-card a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .contact-card a:hover {
            color: var(--secondary);
        }

        /* Cart Sidebar */
        .cart-sidebar {
            position: fixed;
            top: 0;
            right: -400px;
            width: 400px;
            height: 100vh;
            background: white;
            box-shadow: -5px 0 15px rgba(0,0,0,0.2);
            z-index: 2000;
            transition: right 0.3s;
            display: flex;
            flex-direction: column;
        }

        .cart-sidebar.open {
            right: 0;
        }

        .cart-header {
            background: var(--primary);
            color: white;
            padding: 1.5rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .close-cart {
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .cart-items {
            flex: 1;
            overflow-y: auto;
            padding: 1rem;
        }

        .cart-item {
            display: flex;
            gap: 1rem;
            padding: 1rem;
            border-bottom: 1px solid #eee;
            align-items: center;
        }

        .cart-item img {
            width: 80px;
            height: 80px;
            object-fit: cover;
            border-radius: 8px;
        }

        .cart-item-details {
            flex: 1;
        }

        .cart-item-title {
            font-weight: bold;
            color: var(--primary);
            margin-bottom: 0.3rem;
        }

        .cart-item-price {
            color: var(--secondary);
            font-weight: bold;
        }

        .remove-item {
            background: #e74c3c;
            color: white;
            border: none;
            padding: 0.5rem;
            border-radius: 5px;
            cursor: pointer;
        }

        .cart-footer {
            padding: 1.5rem;
            border-top: 2px solid #eee;
            background: #f8f9fa;
        }

        .cart-total {
            display: flex;
            justify-content: space-between;
            font-size: 1.3rem;
            font-weight: bold;
            margin-bottom: 1rem;
            color: var(--primary);
        }

        .checkout-btn {
            width: 100%;
            padding: 1rem;
            background: var(--success);
            color: white;
            border: none;
            border-radius: 8px;
            font-size: 1.1rem;
            cursor: pointer;
            transition: background 0.3s;
        }

        .checkout-btn:hover {
            background: #229954;
        }

        .overlay {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.5);
            z-index: 1500;
            display: none;
        }

        .overlay.show {
            display: block;
        }

        /* Footer */
        footer {
            background: var(--dark);
            color: white;
            text-align: center;
            padding: 2rem;
        }

        .social-links {
            margin-top: 1rem;
            display: flex;
            justify-content: center;
            gap: 1.5rem;
        }

        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--secondary);
        }

        /* Animations */
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 968px) {
            .location-grid {
                grid-template-columns: 1fr;
            }
            
            .map-container {
                min-height: 300px;
            }
            
            .map-container iframe {
                min-height: 300px;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .cart-sidebar {
                width: 100%;
                right: -100%;
            }

            .location-info {
                padding: 2rem;
            }
        }

        /* Notification */
        .notification {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--success);
            color: white;
            padding: 1rem 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
            z-index: 3000;
            transform: translateX(400px);
            transition: transform 0.3s;
        }

        .notification.show {
            transform: translateX(0);
        }

        /* Floating Map Button */
        .floating-map-btn {
            position: fixed;
            bottom: 30px;
            left: 30px;
            background: var(--map-blue);
            color: white;
            width: 60px;
            height: 60px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.5rem;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
            cursor: pointer;
            z-index: 999;
            transition: all 0.3s;
            text-decoration: none;
        }

        .floating-map-btn:hover {
            transform: scale(1.1) rotate(10deg);
            background: #3367d6;
            box-shadow: 0 6px 20px rgba(66, 133, 244, 0.5);
        }

        .floating-map-btn::after {
            content: 'Ver ubicación';
            position: absolute;
            left: 70px;
            background: rgba(0,0,0,0.8);
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 5px;
            font-size: 0.9rem;
            white-space: nowrap;
            opacity: 0;
            pointer-events: none;
            transition: opacity 0.3s;
        }

        .floating-map-btn:hover::after {
            opacity: 1;
        }
    </style>
</head>
<body>

    <!-- Header -->
    <header>
        <nav>
            <div class="logo">
                <i class="fas fa-cubes"></i>
                <span>MIPYME Aportando al Futuro</span>
            </div>
            <ul class="nav-links">
                <li><a href="#inicio">Inicio</a></li>
                <li><a href="#productos">Productos</a></li>
                <li><a href="#nosotros">Nosotros</a></li>
                <li><a href="#ubicacion">Ubicación</a></li>
                <li><a href="#contacto">Contacto</a></li>
                <li class="cart-icon" onclick="toggleCart()">
                    <i class="fas fa-shopping-cart"></i>
                    <span class="cart-count" id="cartCount">0</span>
                </li>
            </ul>
        </nav>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="inicio">
        <div class="hero-content">
            <h1>Calidad que Construye el Futuro</h1>
            <p>Bloques y Losas de Hormigón de Alta Resistencia</p>
            <a href="#productos" class="cta-button">Ver Productos</a>
        </div>
    </section>

    <!-- Stats Section -->
    <section class="stats">
        <div class="stats-container">
            <div class="stat-item">
                <span class="stat-number">4+</span>
                <span class="stat-label">Años de Experiencia</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">50,000+</span>
                <span class="stat-label">Bloques Producidos</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">10,000+</span>
                <span class="stat-label">Losas Producidas</span>
            </div>
            <div class="stat-item">
                <span class="stat-number">100%</span>
                <span class="stat-label">Calidad Garantizada</span>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="productos">
        <h2 class="section-title">Nuestros Productos</h2>
        <div class="products-grid">
            
            <!-- Producto 1: Bloque 15x45x20 -->
            <div class="product-card">
                <span class="product-badge">LÍDER</span>
                <img src="Bloques 1.jpg" alt="Bloque 15x45x20" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">Bloque de Hormigón</h3>
                    <p class="product-specs">Medidas: 15 x 45 x 20 cm<br>Alta resistencia y durabilidad</p>
                    <div class="product-price">$330 <span>CUP</span></div>
                    
                    <div class="quantity-selector">
                        <button class="qty-btn" onclick="updateQty('prod1', -1)">-</button>
                        <input type="number" class="qty-input" id="qty-prod1" value="1" min="1">
                        <button class="qty-btn" onclick="updateQty('prod1', 1)">+</button>
                    </div>
                    
                    <button class="add-to-cart" onclick="addToCart('Bloque 15x45x20', 330, 'bloques 1.jpg', 'prod1')">
                        <i class="fas fa-cart-plus"></i> Añadir al Carrito
                    </button>
                </div>
            </div>

            <!-- Producto 2: Bloque 10x45x20 -->
            <div class="product-card">
                <img src="bloques 15.jpg" alt="Bloque 10x45x20" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">Bloque de Hormigón</h3>
                    <p class="product-specs">Medidas: 10 x 45 x 20 cm<br>Ideal para construcciones livianas</p>
                    <div class="product-price">$300 <span>CUP</span></div>
                    
                    <div class="quantity-selector">
                        <button class="qty-btn" onclick="updateQty('prod2', -1)">-</button>
                        <input type="number" class="qty-input" id="qty-prod2" value="1" min="1">
                        <button class="qty-btn" onclick="updateQty('prod2', 1)">+</button>
                    </div>
                    
                    <button class="add-to-cart" onclick="addToCart('Bloque 10x45x20', 300, 'bloques 15.jpg', 'prod2')">
                        <i class="fas fa-cart-plus"></i> Añadir al Carrito
                    </button>
                </div>
            </div>

            <!-- Producto 3: Losa de Granito 40x40 -->
            <div class="product-card">
                <img src="https://kimi-web-img.moonshot.cn/img/s.alicdn.com/d1fb4a8fb0729703e963a8731d4fa2f3849e75be.jpg" alt="Losa Granito 40x40" class="product-image">
                <div class="product-info">
                    <h3 class="product-title">Losa de Granito</h3>
                    <p class="product-specs">Medidas: 40 x 40 cm<br>Acabado premium para exteriores</p>
                    <div class="product-price">$240 <span>CUP</span></div>
                    
                    <div class="quantity-selector">
                        <button class="qty-btn" onclick="updateQty('prod3', -1)">-</button>
                        <input type="number" class="qty-input" id="qty-prod3" value="1" min="1">
                        <button class="qty-btn" onclick="updateQty('prod3', 1)">+</button>
                    </div>
                    
                    <button class="add-to-cart" onclick="addToCart('Losa Granito 40x40', 240, 'https://kimi-web-img.moonshot.cn/img/s.alicdn.com/d1fb4a8fb0729703e963a8731d4fa2f3849e75be.jpg', 'prod3')">
                        <i class="fas fa-cart-plus"></i> Añadir al Carrito
                    </button>
                </div>
            </div>

        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="nosotros">
        <div class="about-content">
            <div class="about-text">
                <h2>Sobre Nosotros</h2>
                <p><strong>MIPYME Aportando al Futuro S.R.L</strong> es una empresa dedicada a la producción de materiales de construcción de alta calidad. Con más de 4 años de experiencia en el sector, nos hemos consolidado como referentes en la producción de bloques y losas de hormigón.</p>
                <p>Nuestra planta de producción cuenta con equipo comprometido que garantiza la calidad de cada pieza fabricada. Hemos producido más de <strong>50,000 bloques</strong> y <strong>10,000 losas</strong>, contribuyendo a la construcción de hogares y proyectos en toda la región.</p>
                <p>Ubicados en el Reparto Residencial Almendares, estamos estratégicamente posicionados para atender sus necesidades de construcción con puntualidad y profesionalismo.</p>
            </div>
            <div class="about-image">
                <img src="Bloques 2.jpg" alt="Nuestra Fábrica">
            </div>
        </div>
    </section>

    <!-- Location Section with Google Maps -->
    <section class="location-section" id="ubicacion">
        <div class="location-container">
            <h2 class="section-title">Nuestra Ubicación</h2>
            
            <div class="location-grid">
                <!-- Google Maps Embed -->
                <div class="map-container">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d2595.8142300264653!2d-82.40520327744304!3d23.059153106264635!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e0!3m2!1ses!2sus!4v1772483434556!5m2!1ses!2sus" width="600" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>

                <!-- Location Info -->
                <div class="location-info">
                    <div class="location-header">
                        <div class="location-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="location-title">
                            <h3>Encuéntranos</h3>
                            <p>Boyeros, La Habana</p>
                        </div>
                    </div>

                    <div class="address-details">
                        <h4><i class="fas fa-building"></i> Dirección Exacta</h4>
                        <p>
                            Calle Sur (Calle 4)<br>
                            Reparto Residencial Almendares<br>
                            Reloj Club, Boyeros<br>
                            La Habana, Cuba
                        </p>
                    </div>

                    <div class="address-details" style="border-left-color: var(--secondary);">
                        <h4><i class="fas fa-clock"></i> Horario de Atención</h4>
                        <p>
                            <strong>Lunes a Viernes:</strong> 8:00 AM - 5:00 PM<br>
                            <strong>Sábados:</strong> 8:00 AM - 12:00 PM<br>
                            <strong>Domingos:</strong> Cerrado
                        </p>
                    </div>

                    <div class="map-buttons">
                        <a href="https://www.google.com/maps/dir/?api=1&destination=23.05850° N, 82.40596° W" target="_blank" class="map-btn btn-primary-map">
                            <i class="fas fa-directions"></i>
                            Cómo Llegar (Google Maps)
                        </a>
                        
                        <a href="https://www.google.com/maps/search/?api=1&query=23.05850° N, 82.40596° W" target="_blank" class="map-btn btn-secondary-map">
                            <i class="fas fa-expand"></i>
                            Ver Mapa Grande
                        </a>

                        <a href="https://wa.me/5350995323?text=Hola,%20quiero%20información%20sobre%20cómo%20llegar%20a%20su%20empresa" target="_blank" class="map-btn btn-secondary-map">
                            <i class="fab fa-whatsapp"></i>
                            Solicitar Indicaciones por WhatsApp
                        </a>
                    </div>

                    <div class="hours-badge">
                        <i class="fas fa-check-circle"></i>
                        Fábrica operando normalmente
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contacto">
        <div class="contact-container">
            <h2 class="section-title" style="color: white;">Contacto</h2>
            <div class="contact-grid">
                <div class="contact-card">
                    <i class="fas fa-map-marker-alt contact-icon"></i>
                    <h3>Dirección</h3>
                    <p>Calle Sur, Calle 4<br>Reparto Residencial Almendares<br>Reloj Club, Boyeros</p>
                </div>
                <div class="contact-card">
                    <i class="fas fa-phone-alt contact-icon"></i>
                    <h3>Área Comercial</h3>
                    <p><a href="tel:+5350995323">+53 50995323</a><br>Ventas y Cotizaciones</p>
                </div>
                <div class="contact-card">
                    <i class="fas fa-industry contact-icon"></i>
                    <h3>Área Producción</h3>
                    <p><a href="tel:+5350992348">+53 50992348</a><br>Consultas Técnicas</p>
                </div>
                <div class="contact-card">
                    <i class="fas fa-envelope contact-icon"></i>
                    <h3>Correo Electrónico</h3>
                    <p><a href="mailto:osmany2501@gmail.com">osmany2501@gmail.com</a><br>Escríbanos anytime</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2024 MIPYME Aportando al Futuro. Todos los derechos reservados.</p>
        <div class="social-links">
            <a href="#"><i class="fab fa-facebook"></i></a>
            <a href="https://wa.me/5350995323"><i class="fab fa-whatsapp"></i></a>
            <a href="mailto:osmany2501@gmail.com"><i class="fas fa-envelope"></i></a>
        </div>
    </footer>

    <!-- Floating Map Button -->
    <a href="#ubicacion" class="floating-map-btn" title="Ver nuestra ubicación">
        <i class="fas fa-map-marker-alt"></i>
    </a>

    <!-- Cart Sidebar -->
    <div class="overlay" id="overlay" onclick="toggleCart()"></div>
    <div class="cart-sidebar" id="cartSidebar">
        <div class="cart-header">
            <h3><i class="fas fa-shopping-cart"></i> Tu Carrito</h3>
            <button class="close-cart" onclick="toggleCart()"><i class="fas fa-times"></i></button>
        </div>
        <div class="cart-items" id="cartItems">
            <!-- Items se agregan dinámicamente -->
        </div>
        <div class="cart-footer">
            <div class="cart-total">
                <span>Total:</span>
                <span id="cartTotal">$0 CUP</span>
            </div>
            <button class="checkout-btn" onclick="checkout()">
                <i class="fas fa-whatsapp"></i> Solicitar Pedido por WhatsApp
            </button>
        </div>
    </div>

    <!-- Notification -->
    <div class="notification" id="notification">
        Producto añadido al carrito
    </div>

    <script>
        let cart = [];
        
        function updateQty(productId, change) {
            const input = document.getElementById('qty-' + productId);
            let newVal = parseInt(input.value) + change;
            if (newVal < 1) newVal = 1;
            input.value = newVal;
        }

        function addToCart(name, price, image, productId) {
            const qty = parseInt(document.getElementById('qty-' + productId).value);
            const existingItem = cart.find(item => item.name === name);
            
            if (existingItem) {
                existingItem.qty += qty;
            } else {
                cart.push({ name, price, image, qty });
            }
            
            updateCart();
            showNotification();
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCart();
        }

        function updateCart() {
            const cartItems = document.getElementById('cartItems');
            const cartCount = document.getElementById('cartCount');
            const cartTotal = document.getElementById('cartTotal');
            
            cartItems.innerHTML = '';
            let total = 0;
            let count = 0;
            
            cart.forEach((item, index) => {
                total += item.price * item.qty;
                count += item.qty;
                
                cartItems.innerHTML += `
                    <div class="cart-item">
                        <img src="${item.image}" alt="${item.name}">
                        <div class="cart-item-details">
                            <div class="cart-item-title">${item.name}</div>
                            <div class="cart-item-price">$${item.price} x ${item.qty}</div>
                        </div>
                        <button class="remove-item" onclick="removeFromCart(${index})">
                            <i class="fas fa-trash"></i>
                        </button>
                    </div>
                `;
            });
            
            cartCount.textContent = count;
            cartTotal.textContent = '$' + total + ' CUP';
        }

        function toggleCart() {
            document.getElementById('cartSidebar').classList.toggle('open');
            document.getElementById('overlay').classList.toggle('show');
        }

        function showNotification() {
            const notif = document.getElementById('notification');
            notif.classList.add('show');
            setTimeout(() => notif.classList.remove('show'), 3000);
        }

        function checkout() {
            if (cart.length === 0) {
                alert('Tu carrito está vacío');
                return;
            }
            
            let message = '¡Hola! Quiero realizar el siguiente pedido:%0A%0A';
            let total = 0;
            
            cart.forEach(item => {
                message += `• ${item.name} (${item.qty} unidades) - $${item.price * item.qty} CUP%0A`;
                total += item.price * item.qty;
            });
            
            message += `%0ATotal: $${total} CUP%0A%0AGracias.`;
            
            window.open(`https://wa.me/5350995323?text=${message}`, '_blank');
        }

        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                }
            });
        });

        // Show/hide floating map button based on scroll
        window.addEventListener('scroll', function() {
            const floatingBtn = document.querySelector('.floating-map-btn');
            const locationSection = document.getElementById('ubicacion');
            const rect = locationSection.getBoundingClientRect();
            
            if (rect.top < window.innerHeight && rect.bottom > 0) {
                floatingBtn.style.opacity = '0';
                floatingBtn.style.pointerEvents = 'none';
            } else {
                floatingBtn.style.opacity = '1';
                floatingBtn.style.pointerEvents = 'all';
            }
        });
    </script>

</body>
</html>
