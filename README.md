<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    #<title>NEXOVA DIGITAL</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Montserrat:wght@300;400;600&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --blue-pastel: #a6d8f5;
            --gray-pastel: #a1a1a1;
            --dark-gray: #555555;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            background-color: white;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
            opacity: 0;
            transform: translateY(20px);
            animation: fadeUp 1s ease-out forwards;
        }
        
        header {
            text-align: center;
            margin-bottom: 50px;
            opacity: 0;
            animation: fadeIn 1.5s ease-out 0.2s forwards;
        }
        
        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.8rem;
            margin-bottom: 10px;
            color: #333;
            position: relative;
            display: inline-block;
        }
        
        h1::after {
            content: '';
            position: absolute;
            width: 80px;
            height: 3px;
            background-color: var(--blue-pastel);
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
        }
        
        h2 {
            font-family: 'Montserrat', sans-serif;
            font-weight: 400;
            font-size: 1.3rem;
            color: var(--gray-pastel);
            margin-top: 20px;
        }
        
        .services {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-bottom: 60px;
        }
        
        .service-card {
            background-color: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            padding: 30px;
            text-align: center;
            width: 300px;
            border: 1px solid #f0f0f0;
            transition: transform 0.3s, box-shadow 0.3s;
            opacity: 0;
            transform: translateY(20px);
            cursor: pointer;
        }

        .service-card:hover,
        .service-card:focus {
            transform: scale(1.05);
            box-shadow: 0 15px 30px rgba(166, 216, 245, 0.3);
        }

        .service-card:active {
            transform: scale(1.1);
            box-shadow: 0 20px 40px rgba(166, 216, 245, 0.4);
        }
        
        .service-card h3 {
            font-family: 'Playfair Display', serif;
            margin: 15px 0;
            font-size: 1.4rem;
        }
        
        .service-card .price {
            font-size: 1.5rem;
            color: var(--dark-gray);
            font-weight: 600;
            margin: 15px 0;
        }
        
        .service-card .description {
            font-size: 0.9rem;
            color: var(--gray-pastel);
            margin-bottom: 20px;
        }
        
        .icon {
            font-size: 2.5rem;
            color: var(--blue-pastel);
            margin-bottom: 15px;
        }
        
        .image-placeholder {
            width: 100%;
            height: 150px;
            background-color: #f5f5f5;
            margin: 20px 0;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--gray-pastel);
            border: 1px dashed var(--blue-pastel);
            border-radius: 5px;
        }
        
        .cta {
            text-align: center;
            background-color: #f9f9f9;
            padding: 50px 20px;
            border-radius: 10px;
            margin: 40px 0;
            opacity: 0;
            animation: fadeIn 1.5s ease-out 1s forwards;
        }
        
        .cta h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            margin-bottom: 20px;
        }
        
        .cta-button {
            display: inline-block;
            background-color: var(--blue-pastel);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: 600;
            text-decoration: none;
            margin-top: 20px;
            transition: transform 0.3s, background-color 0.3s;
            box-shadow: 0 4px 8px rgba(166, 216, 245, 0.3);
        }
        
        .cta-button:hover {
            background-color: #8cc5e7;
            transform: translateY(-3px);
        }
        
        .contact {
            text-align: center;
            margin-top: 40px;
            opacity: 0;
            animation: fadeIn 1.5s ease-out 1.5s forwards;
        }
        
        .contact-icons {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        .contact-icons a {
            color: var(--blue-pastel);
            font-size: 1.5rem;
            transition: transform 0.3s, color 0.3s;
        }
        
        .contact-icons a:hover {
            color: #8cc5e7;
            transform: translateY(-3px);
        }
        
        @keyframes fadeIn {
            from {
                opacity: 0;
            }
            to {
                opacity: 1;
            }
        }
        
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(20px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.1rem;
            }
            
            .services {
                flex-direction: column;
                align-items: center;
            }
        }

        .testimonials {
            background-color: #f9f9f9;
            padding: 50px 20px;
            border-radius: 10px;
            margin: 40px 0;
            text-align: center;
            display: none; /* Initially hidden */
        }

        .testimonial {
            position: relative;
            margin-bottom: 30px;
        }

        .testimonial p {
            font-size: 1rem;
            color: #555;
        }

        .stars {
            color: #ffd700;
            font-size: 1.5rem;
        }

        .testimonial-form {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .testimonial-form input[type="text"],
        .testimonial-form textarea {
            width: 100%;
            max-width: 600px;
            margin-bottom: 20px;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
        }

        .testimonial-form .stars-input {
            display: flex;
            gap: 5px;
            margin-bottom: 20px;
        }

        .testimonial-form .stars-input input {
            display: none;
        }

        .testimonial-form .stars-input label {
            font-size: 1.5rem;
            color: #ddd;
            cursor: pointer;
        }

        .testimonial-form .stars-input input:checked ~ label,
        .testimonial-form .stars-input input:checked ~ label ~ label {
            color: #ffd700;
        }

        .testimonial-form button {
            background-color: var(--blue-pastel);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .testimonial-form button:hover {
            background-color: #8cc5e7;
        }

        .edit-delete-buttons {
            display: none; /* Initially hidden */
            position: absolute;
            top: 10px;
            right: 10px;
            gap: 10px;
        }

        .edit-delete-buttons button {
            background-color: var(--blue-pastel);
            border: none;
            cursor: pointer;
            color: white;
            font-size: 1rem;
            padding: 5px 10px;
            border-radius: 5px;
            transition: background-color 0.3s;
        }

        .edit-delete-buttons button:hover {
            background-color: #8cc5e7;
        }

        .testimonials-button {
            background-color: var(--blue-pastel);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s;
            margin-bottom: 20px;
        }

        .testimonials-button:hover {
            background-color: #8cc5e7;
        }

        .logo {
            position: absolute;
            top: 10px;
            right: 20px;
            width: 100px;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <img src="LOGO SIN FONDO.png" alt="NEXOVA DIGITAL Logo" class="logo">
            <h1>NEXOVA DIGITAL</h1>
            <h2>Diseño de Páginas Web, Sitios Web y Apps Web Básicas</h2>
        </header>
        
        <div class="services">
            <div class="service-card" id="card1">
                <div class="icon">
                    <i class="fas fa-file-code"></i>
                </div>
                <h3>Página Web Básica</h3>
                <p class="description">Ideal para una landing page o página sencilla.</p>
                <div class="image-placeholder">
                    <img src="paginaweb.imagen.jpeg" alt="Custom Face Socks" style="width: 100%; height: 100%; object-fit: cover; border-radius: 5px;">
                </div>
                <p class="price">Desde 100€-300€</p>
            </div>
            
            <div class="service-card" id="card2">
                <div class="icon">
                    <i class="fas fa-sitemap"></i>
                </div>
                <h3>Sitio Web Completo</h3>
                <p class="description">Perfecto para pequeñas empresas o proyectos personales (hasta 5 páginas).</p>
                <div class="image-placeholder">
                    <img src="sitioweb.imagen" alt="Custom Face Socks" style="width: 100%; height: 100%; object-fit: cover; border-radius: 5px;">
                </div>
                <p class="price">Desde 300€-500€</p>
            </div>
            
            <div class="service-card" id="card3">
                <div class="icon">
                    <i class="fas fa-mobile-alt"></i>
                </div>
                <h3>App Web Básica</h3>
                <p class="description">Para llevar tu idea a la web con funcionalidades básicas.</p>
                <div class="image-placeholder">
                    <img src="appweb.imagen" alt="Custom Face Socks" style="width: 100%; height: 100%; object-fit: cover; border-radius: 5px;">
                </div>
                <p class="price">Desde 400€-600€</p>
            </div>

            <div class="service-card" id="card4">
                <div class="icon">
                    <i class="fas fa-tools"></i>
                </div>
                <h3>Mantenimiento Mensual</h3>
                <p class="description">De preferencia para mantener tu sitio web actualizado y seguro.</p>
                <div class="image-placeholder">
                    <img src="mantenimiento.imagen" alt="Mantenimiento Mensual" style="width: 100%; height: 100%; object-fit: cover; border-radius: 5px;">
                </div>
                <p class="price">80€</p>
            </div>
            
            <div class="service-card" id="card5">
                <div class="icon">
                    <i class="fas fa-redo"></i>
                </div>
                <h3>Rediseño de Página</h3>
                <p class="description">Actualiza el diseño de tu página web para una apariencia moderna.</p>
                <div class="image-placeholder">
                    <img src="rediseño.imagen" alt="Rediseño de Página" style="width: 100%; height: 100%; object-fit: cover; border-radius: 5px;">
                </div>
                <p class="price">250€</p>
            </div>
        </div>
        
        <div class="cta">
            <h3>¡Haz crecer tu negocio online hoy mismo!</h3>
            <p>Da el primer paso hacia una presencia online profesional y atractiva.</p>
            <a href="#" class="cta-button">Contacta para más información</a>
        </div>

        <button class="testimonials-button" onclick="toggleTestimonials()">Testimonios de Clientes</button>
        <div class="testimonials">
            <div class="testimonial">
                <p><strong>servicio</strong></p>
                <p>"Excelente servicio y atención. Muy satisfecho con el resultado."</p>
                <div class="stars">
                    ★★★★☆
                </div>
                <div class="edit-delete-buttons">
                    <button onclick="editTestimonial(this)">Editar</button>
                    <button onclick="deleteTestimonial(this)">Eliminar</button>
                </div>
            </div>
            <div class="testimonial">
                <p><strong>calidad-precio/strong></p>
                <p>"Buena relación calidad-precio. Recomendado."</p>
                <div class="stars">
                    ★★★★★
                </div>
                <div class="edit-delete-buttons">
                   
                    <button onclick="deleteTestimonial(this)">Eliminar</button>
                </div>
            </div>
            <div class="testimonial-form">
                <h4>Deja tu Testimonio</h4>
                <input type="text" placeholder="Tu nombre de usuario" required>
                <textarea placeholder="Escribe tu testimonio aquí..." required></textarea>
                <div class="stars-input">
                    <input type="radio" id="star5" name="rating" value="5"><label for="star5">★</label>
                    <input type="radio" id="star4" name="rating" value="4"><label for="star4">★</label>
                    <input type="radio" id="star3" name="rating" value="3"><label for="star3">★</label>
                    <input type="radio" id="star2" name="rating" value="2"><label for="star2">★</label>
                    <input type="radio" id="star1" name="rating" value="1"><label for="star1">★</label>
                </div>
                <input type="file" accept="image/*">
                <button type="button" onclick="submitTestimonial()">Enviar Testimonio</button>
            </div>
        </div>
        
        <div class="contact">
            <h3>Datos de contacto</h3>
            <div class="contact-icons">
                <a href="mailto:digitalxenova@gmail.com" title="Email"><i class="fas fa-envelope"></i></a>
                <a href="https://wa.me/+573226429963" title="WhatsApp"><i class="fas fa-phone"></i></a>
                <a href="https://www.instagram.com/nexova_digital?igsh=bWZsYWpkcDZodnBh" title="Instagram"><i class="fab fa-instagram"></i></a>
                <a href="#" title="Facebook"><i class="fab fa-facebook"></i></a>
                <a href="#" title="TikTok"><i class="fab fa-tiktok"></i></a>
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            // Animación de entrada para las tarjetas de servicios
            const cards = document.querySelectorAll('.service-card');
            
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.style.animation = `fadeUp 0.8s ease-out ${0.3 + index * 0.2}s forwards`;
                }, 100);
            });
            
            // Función para permitir añadir imágenes (simulación)
            const imagePlaceholders = document.querySelectorAll('.image-placeholder');
            
            imagePlaceholders.forEach(placeholder => {
                placeholder.addEventListener('click', function() {
                    alert('Aquí podrías implementar un selector de imágenes para que el usuario pueda subir sus propias imágenes.');
                });
            });
        });

        function editTestimonial(button) {
            const testimonial = button.closest('.testimonial');
            const username = testimonial.querySelector('p strong').innerText;
            const text = testimonial.querySelectorAll('p')[1].innerText;
            const stars = testimonial.querySelector('.stars').innerText.length;
            const form = document.querySelector('.testimonial-form');
            form.querySelector('input[type="text"]').value = username;
            form.querySelector('textarea').value = text;
            form.querySelector(`input[name="rating"][value="${stars}"]`).checked = true;
            form.scrollIntoView({ behavior: 'smooth' });
            testimonial.remove();
        }

        function deleteTestimonial(button) {
            const testimonial = button.closest('.testimonial');
            testimonial.remove();
        }

        function toggleTestimonials() {
            const testimonials = document.querySelector('.testimonials');
            testimonials.style.display = testimonials.style.display === 'none' ? 'block' : 'none';
        }

        function submitTestimonial() {
            const form = document.querySelector('.testimonial-form');
            const username = form.querySelector('input[type="text"]').value;
            const testimonialText = form.querySelector('textarea').value;
            const rating = form.querySelector('input[name="rating"]:checked').value;
            const fileInput = form.querySelector('input[type="file"]');
            const testimonialContainer = document.createElement('div');
            testimonialContainer.classList.add('testimonial');
            testimonialContainer.innerHTML = `
                <p><strong>${username}</strong></p>
                <p>${testimonialText}</p>
                ${fileInput.files.length > 0 ? `<img src="${URL.createObjectURL(fileInput.files[0])}" alt="User Image" style="width: 100px; height: 100px; object-fit: cover; border-radius: 5px;">` : ''}
                <div class="stars">${'★'.repeat(rating)}${'☆'.repeat(5 - rating)}</div>
                <div class="edit-delete-buttons" style="display: flex;">
                    <button onclick="editTestimonial(this)">Editar</button>
                    <button onclick="deleteTestimonial(this)">Eliminar</button>
                </div>
            `;
            document.querySelector('.testimonials').appendChild(testimonialContainer);
            form.reset();
        }
    </script>
</body>
</html>
