<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Minha Viagem - Explore o Mundo</title>
    <style>
        /* RESET BÁSICO */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth; /* Deixa a rolagem interna suave */
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #333;
        }

        /* HEADER & NAV */
        header {
            background-color: #ffffff;
            position: fixed; /* Fixa o menu no topo ao rolar a página */
            top: 0;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            color: #2c3e50;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 20px;
        }

        nav a {
            text-decoration: none;
            color: #555;
            font-weight: 600;
            padding: 8px 12px;
            border-radius: 4px;
            /* Transição suave exigida no requisito 3.2 */
            transition: background-color 0.3s ease, color 0.3s ease; 
        }

        /* Efeito Hover na Navegação (Requisito 3.1) */
        nav a:hover {
            background-color: #3498db;
            color: #ffffff;
        }

        /* BANNER PRINCIPAL (Requisito 1.1 e 1.3) */
        .banner {
            height: 100vh; /* Ocupa a tela inteira inicialmente */
            background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR5ajESGeJVA7mabsAjI5AdMHA-IFdfspOxgW-sX-i-RQ&s=10'); /* Imagem de vilarejo europeu */
            background-size: cover;
            background-position: center;
            background-attachment: fixed; /* Efeito Parallax simples */
            display: flex;
            align-items: center;
            justify-content: center;
            padding-top: 80px; /* Evita que o header fixo cubra o conteúdo */
        }

        /* Overlay escuro para dar leitura ao texto (Requisito 1.2) */
        .banner-overlay {
            background-color: rgba(0, 0, 0, 0.55); 
            padding: 40px;
            border-radius: 8px;
            text-align: center;
            color: #ffffff;
            max-width: 800px;
            margin: 20px;
        }

        .banner-overlay h1 {
            font-size: 2.8rem;
            margin-bottom: 15px;
        }

        .banner-overlay p {
            font-size: 1.2rem;
            margin-bottom: 25px;
        }

        /* Botão do Banner com Hover */
        .btn-banner {
            display: inline-block;
            padding: 12px 24px;
            background-color: #e74c3c;
            color: white;
            text-decoration: none;
            font-weight: bold;
            border-radius: 5px;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }

        .btn-banner:hover {
            background-color: #c0392b;
            transform: translateY(-2px); /* Pequeno efeito visual de elevação */
        }

        /* SEÇÕES DE CONTEÚDO */
        .conteudo-section {
            padding: 80px 20px;
            min-height: 50vh;
        }

        .bg-light {
            background-color: #f9f9f9;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
        }

        .container h2 {
            font-size: 2rem;
            margin-bottom: 30px;
            color: #2c3e50;
            border-bottom: 3px solid #3498db;
            display: inline-block;
            padding-bottom: 5px;
        }

        /* Layout Responsivo Simples */
        .grid-layout {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            margin-bottom: 40px;
        }

        .card {
            flex: 1 1 300px;
            background: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.05);
        }

        .card h3, .sidebar-info h3 {
            margin-bottom: 15px;
            color: #34495e;
        }

        .sidebar-info {
            flex: 1 1 250px;
            background-color: #e1f5fe;
            padding: 25px;
            border-radius: 8px;
            border-left: 5px solid #0288d1;
        }

        /* LINK VOLTAR AO TOPO (Requisito 2.1) */
        .back-to-top {
            display: inline-block;
            margin-top: 20px;
            color: #3498db;
            text-decoration: none;
            font-weight: bold;
            transition: color 0.2s ease;
        }

        .back-to-top:hover {
            color: #2980b9;
            text-decoration: underline;
        }

        /* RODAPÉ */
        footer {
            background-color: #2c3e50;
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header id="topo">
        <div class="header-container">
            <div class="logo">✈️ MinhaViagem</div>
            <nav aria-label="Navegação principal">
                <ul>
                    <li><a href="#trip-me">TripMe</a></li>
                    <li><a href="#meet-us">NosEncontre</a></li>
                    <li><a href="#advice">Conselhos</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        
        <section id="trip-me" class="banner">
            <div class="banner-overlay">
                <h1>Descubra o Charme dos Vilarejos Europeus</h1>
                <p>Encontre o destino perfeito para a sua próxima grande aventura remota.</p>
                <a href="#advice" class="btn-banner">Ver Dicas de Viagem</a>
            </div>
        </section>

        <section id="meet-us" class="conteudo-section">
            <div class="container">
                <h2>Nos Encontre (MeetUs)</h2>
                <div class="grid-layout">
                    <article class="card">
                        <h3>Nossa Sede</h3>
                        <p>Localizada no coração de uma vila histórica, prontos para planejar seu roteiro personalizado.</p>
                    </article>
                    <aside class="sidebar-info">
                        <h3>Atendimento</h3>
                        <p>Segunda a Sexta: 9h às 18h</p>
                        <p>Suporte 100% online para viajantes.</p>
                    </aside>
                </div>
                <a href="#topo" class="back-to-top" aria-label="Voltar ao topo">Voltar ao topo ↑</a>
            </div>
        </section>

        <section id="advice" class="conteudo-section bg-light">
            <div class="container">
                <h2>Conselhos para Viajantes (Advice)</h2>
                <div class="grid-layout">
                    <article class="card">
                        <h3>1. Planeje com Antecedência</h3>
                        <p>Vilarejos remotos costumam ter transporte limitado. Verifique horários de trens e ônibus locais.</p>
                    </article>
                    <article class="card">
                        <h3>2. Respeite a Cultura Local</h3>
                        <p>A imersão cultural fica muito melhor quando você consome do comércio local e respeita as tradições.</p>
                    </article>
                </div>
                <a href="#topo" class="back-to-top" aria-label="Voltar ao topo">Voltar ao topo ↑</a>
            </div>
        </section>

    </main>

    <footer>
        <p>&copy; 2026 MinhaViagem. Desenvolvido com foco em HTML Semântico e CSS.</p>
    </footer>

</body>
</html>
