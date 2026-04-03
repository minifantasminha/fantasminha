# fantasminha
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <!-- ✅ MUDE AQUI O TÍTULO DO SEU SITE -->
    <title>WebMaster Pro - Criação de Sites Profissionais</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Criação de sites profissionais com design moderno e responsivo.">
    
    <style>
        /* DESIGN BRANCO COM AZUL CLARO */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #f8f9ff 0%, #ffffff 100%);
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* HEADER */
        header {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(59,130,246,0.1);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        /* ✅ MUDE AQUI SEU LOGO/NOME */
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #3b82f6;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: #1d4ed8;
        }

        /* HERO SECTION */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 2rem;
            position: relative;
            overflow: hidden;
        }

        /* ✅ MUDE AQUI A FOTO DE FUNDO */
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('https://images.unsplash.com/photo-1460925895917-afdab827c52f?ixlib=rb-4.0.3&auto=format&fit=crop&w=2070&q=80') center/cover;
            opacity: 0.1;
            z-index: -1;
        }

        .hero-content h1 {
            font-size: clamp(2.5rem, 5vw, 4rem);
            margin-bottom: 1.5rem;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .hero-content p {
            font-size: 1.3rem;
            margin-bottom: 2rem;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            color: #666;
        }

        .cta-button {
            display: inline-block;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            color: white;
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s;
            box-shadow: 0 10px 30px rgba(59,130,246,0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(59,130,246,0.4);
        }

        /* SERVICES */
        .services {
            padding: 100px 2rem;
            max-width: 1200px;
            margin: 0 auto;
        }

        .section-title {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 4rem;
            color: #1e293b;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .service-card {
            background: white;
            padding: 2.5rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            transition: all 0.3s;
            border: 1px solid rgba(59,130,246,0.1);
        }

        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 60px rgba(59,130,246,0.15);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            border-radius: 20px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1.5rem;
            font-size: 2rem;
            color: white;
        }

        /* PRICING */
        .pricing {
            padding: 100px 2rem;
            background: rgba(59,130,246,0.03);
        }

        .pricing-grid {
            max-width: 1200px;
            margin: 4rem auto 0;
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .price-card {
            background: white;
            padding: 3rem 2rem;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 10px 40px rgba(0,0,0,0.1);
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .price-card.featured {
            transform: scale(1.05);
            background: linear-gradient(135deg, #3b82f6, #60a5fa);
            color: white;
        }

        .price-card.featured .price-amount {
            color: white;
        }

        .price-header {
            margin-bottom: 2rem;
        }

        .price-amount {
            font-size: 3rem;
            font-weight: bold;
            color: #3b82f6;
        }

        .price-period {
            color: #666;
            font-size: 1.1rem;
        }

        /* CONTACT */
        .contact {
            padding: 100px 2rem;
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
        }

        .contact h2 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            color: #1e293b;
        }

        .contact p {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 3rem;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            padding: 1.5rem;
            background: white;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0,0,0,0.1);
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: linear-gradient(45deg, #3b82f6, #60a5fa);
            border-radius: 12px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }

        /* FOOTER */
        footer {
            background: #1e293b;
            color: white;
            text-align: center;
            padding: 3rem 2rem 2rem;
        }

        /* RESPONSIVO */
        @media (max-width: 768px) {
            .nav-links {
                display: none;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
        }

        /* ANIMAÇÕES */
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

        .service-card, .price-card, .contact-item {
            animation: fadeInUp 0.6s ease forwards;
        }
    </style>
</head>
<body>
    <!-- HEADER -->
    <header>
        <nav>
            <!-- ✅ MUDE AQUI SEU NOME/LOGO -->
            <a href="#" class="logo">WebMaster Pro</a>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#services">Serviços</a></li>
                <li><a href="#pricing">Preços</a></li>
                <li><a href="#contact">Contato</a></li>
            </ul>
        </nav>
    </header>

    <!-- HERO -->
    <section id="home" class="hero">
        <div class="hero-content">
            <!-- ✅ MUDE AQUI SEU TÍTULO PRINCIPAL -->
            <h1>Criação de Sites que Vendem</h1>
            <!-- ✅ MUDE AQUI SUA DESCRIÇÃO -->
            <p>Transformamos sua ideia em um site profissional que atrai clientes e gera resultados reais. Design moderno, rápido e otimizado para conversões.</p>
            <!-- ✅ MUDE AQUI SEU WHATSAPP -->
            <a href="https://wa.me/5511999999999?text=Quero%20criar%20meu%20site!" class="cta-button">Fale Comigo Agora</a>
        </div>
    </section>

    <!-- SERVICES -->
    <section id="services" class="services">
        <h2 class="section-title">Nossos Serviços</h2>
        <div class="services-grid">
            <div class="service-card">
                <div class="service-icon">🎨</div>
                <!-- ✅ MUDE AQUI OS SERVIÇOS -->
                <h3>Design Personalizado</h3>
                <p>Sites únicos que representam sua marca com design moderno e responsivo para todos dispositivos.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">⚡</div>
                <h3>Carregamento Rápido</h3>
                <p>Otimização completa para Google com carregamento em menos de 2 segundos.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">📱</div>
                <h3>100% Responsivo</h3>
                <p>Perfeito em celular, tablet e desktop. Seus clientes nunca perdem uma venda.</p>
            </div>
            <div class="service-card">
                <div class="service-icon">🔒</div>
                <h3>Hospedagem Inclusa</h3>
                <p>Hospedagem rápida e segura por 12 meses + domínio .com grátis no 1º ano.</p>
            </div>
        </div>
    </section>

    <!-- PRICING -->
    <section id="pricing" class="pricing">
        <div style="max-width: 800px; margin: 0 auto; text-align: center; padding: 0 2rem;">
            <!-- ✅ MUDE AQUI O TÍTULO DOS PLANOS -->
            <h2 class="section-title" style="color: #1e293b;">Escolha Seu Plano</h2>
            <p style="font-size: 1.2rem; color: #666; margin-bottom: 4rem;">Planos acessíveis com tudo incluso para você começar agora</p>
        </div>
        
        <div class="pricing-grid">
            <!-- ✅ MUDE AQUI OS VALORES E DESCRIÇÕES -->
            <div class="price-card">
                <div class="price-header">
                    <h3>Básico</h3>
                    <div class="price-amount">R$ 497</div>
                    <div class="price-period">uma vez</div>
                </div>
                <ul style="text-align: left; margin-bottom: 2rem;">
                    <li>✅ 1 página inicial</li>
                    <li>✅ Design responsivo</li>
                    <li>✅ Otimização SEO básica</li>
                    <li>✅ 3 revisões</li>
                </ul>
                <a href="https://wa.me/5511999999999" class="cta-button">Quero o Básico</a>
            </div>

            <div class="price-card featured">
                <div class="price-header">
                    <h3>Profissional ⭐</h3>
                    <div class="price-amount">R$ 997</div>
                    <div class="price-period">uma vez</div>
                </div>
                <ul style="text-align: left; margin-bottom: 2rem; color: rgba(255,255,255,0.9);">
                    <li>✅ 5 páginas completas</li>
                    <li>✅ Design premium</li>
                    <li>✅ SEO avançado</li>
                    <li>✅ Hospedagem 12 meses</li>
                    <li>✅ Domínio grátis</li>
                    <li>✅ Suporte 30 dias</li>
                </ul>
                <a href="https://wa.me/5511999999999" class="cta-button" style="background: white; color: #3b82f6;">Quero o Profissional</a>
            </div>

            <div class="price-card">
                <div class="price-header">
                    <h3>Enterprise</h3>
                    <div class="price-amount">R$ 1.997</div>
                    <div class="price-period">uma vez</div>
                </div>
                <ul style="text-align: left; margin-bottom: 2rem;">
                    <li>✅ Site completo ilimitado</li>
                    <li>✅ E-commerce incluso</li>
                    <li>✅ Integração WhatsApp</li>
                    <li>✅ Manutenção 6 meses</li>
                    <li>✅ Treinamento incluso</li>
                </ul>
                <a href="https://wa.me/5511999999999" class="cta-button">Quero o Enterprise</a>
            </div>
        </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact">
        <!-- ✅ MUDE AQUI SUA MENSAGEM FINAL -->
        <h2>Pronto para Transformar seu Negócio?</h2>
        <p>Me chame no WhatsApp e vamos criar o site perfeito para você em até 7 dias!</p>
        
        <div class="contact-info">
            <!-- ✅ MUDE AQUI SEUS DADOS -->
            <div class="contact-item">
                <div class="contact-icon">📱</div>
                <div>
                    <h4>WhatsApp</h4>
                    <a href="https://wa.me/5511999999999" style="color: #3b82f6; font-weight: bold; font-size: 1.1rem;">(11) 99999-9999</a>
                </div>
            </div>
            <div class="contact-item">
                <div class="contact-icon">✉️</div>
                <div>
                    <h4>Email</h4>
                    <a href="mailto:seuemail@exemplo.com" style="color: #3b82f6; font-weight: bold; font-size: 1.1rem;">seuemail@exemplo.com</a>
                </div>
            </div>
        </div>
    </section>

    <!-- FOOTER -->
    <footer>
        <!-- ✅ MUDE AQUI O RODAPÉ -->
        <p>&copy; 2024 WebMaster Pro. Todos os direitos reservados. | Criação de sites profissionais.</p>
    </footer>
</body>
</html>
