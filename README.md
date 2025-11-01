<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README - Café Literário Nelly</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Crimson+Text:wght@400;600&family=Montserrat:wght@300;400;500;600&display=swap');
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        :root {
            --bege-claro: #EAE0D5;
            --bege: #D4C5B9;
            --marrom: #4A3F35;
            --marrom-escuro: #2C2218;
            --verde-suave: #8B9D83;
            --creme: #F5F1E8;
            --branco: #FFFFFF;
        }
        
        body {
            font-family: 'Montserrat', sans-serif;
            line-height: 1.8;
            color: var(--marrom-escuro);
            background: linear-gradient(135deg, var(--creme) 0%, var(--bege-claro) 100%);
            padding: 2rem;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: var(--branco);
            border-radius: 20px;
            box-shadow: 0 20px 80px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        header {
            background: linear-gradient(135deg, var(--marrom-escuro) 0%, var(--marrom) 100%);
            color: var(--bege-claro);
            padding: 4rem 3rem;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        header::before {
            content: '☕';
            position: absolute;
            font-size: 15rem;
            opacity: 0.1;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }
        
        h1 {
            font-family: 'Crimson Text', serif;
            font-size: 3.5rem;
            margin-bottom: 1rem;
            position: relative;
            z-index: 1;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
            font-style: italic;
            position: relative;
            z-index: 1;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 1rem;
            flex-wrap: wrap;
            margin-top: 2rem;
        }
        
        .badge {
            background: var(--verde-suave);
            color: white;
            padding: 0.5rem 1.2rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .content {
            padding: 3rem;
        }
        
        h2 {
            font-family: 'Crimson Text', serif;
            font-size: 2.5rem;
            color: var(--marrom-escuro);
            margin: 3rem 0 1.5rem;
            padding-bottom: 1rem;
            border-bottom: 3px solid var(--verde-suave);
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        h3 {
            font-family: 'Crimson Text', serif;
            font-size: 1.8rem;
            color: var(--marrom);
            margin: 2rem 0 1rem;
        }
        
        p {
            margin-bottom: 1.5rem;
            font-size: 1.05rem;
            text-align: justify;
        }
        
        .feature-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .feature-card {
            background: var(--bege-claro);
            padding: 2rem;
            border-radius: 15px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
        }
        
        .feature-card .icon {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .tech-table {
            width: 100%;
            border-collapse: collapse;
            margin: 2rem 0;
            background: var(--creme);
            border-radius: 10px;
            overflow: hidden;
        }
        
        .tech-table th {
            background: var(--marrom);
            color: var(--bege-claro);
            padding: 1.5rem;
            text-align: left;
            font-weight: 600;
        }
        
        .tech-table td {
            padding: 1.5rem;
            border-bottom: 1px solid var(--bege);
        }
        
        .tech-table tr:last-child td {
            border-bottom: none;
        }
        
        .code-block {
            background: var(--marrom-escuro);
            color: var(--bege-claro);
            padding: 2rem;
            border-radius: 10px;
            overflow-x: auto;
            margin: 1.5rem 0;
            font-family: 'Courier New', monospace;
            font-size: 0.95rem;
            line-height: 1.6;
        }
        
        .color-palette {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 1rem;
            margin: 2rem 0;
        }
        
        .color-box {
            text-align: center;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .color-sample {
            height: 100px;
        }
        
        .color-info {
            background: white;
            padding: 1rem;
            font-size: 0.9rem;
        }
        
        .checklist {
            list-style: none;
            padding-left: 0;
        }
        
        .checklist li {
            padding: 0.8rem 0;
            padding-left: 2.5rem;
            position: relative;
        }
        
        .checklist li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--verde-suave);
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .checklist.future li::before {
            content: '☐';
            color: var(--bege);
        }
        
        .contact-info {
            background: linear-gradient(135deg, var(--verde-suave) 0%, var(--marrom) 100%);
            color: white;
            padding: 3rem;
            border-radius: 15px;
            margin: 3rem 0;
            text-align: center;
        }
        
        .contact-info h3 {
            color: white;
            margin-top: 0;
        }
        
        .contact-info p {
            font-size: 1.1rem;
            margin: 1rem 0;
        }
        
        .author-section {
            background: var(--bege-claro);
            padding: 3rem;
            border-radius: 15px;
            margin: 3rem 0;
            text-align: center;
        }
        
        .author-section h2 {
            border: none;
            justify-content: center;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-top: 2rem;
        }
        
        .social-links a {
            color: var(--marrom-escuro);
            text-decoration: none;
            font-weight: 500;
            padding: 1rem 2rem;
            background: white;
            border-radius: 10px;
            transition: all 0.3s ease;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
        }
        
        .social-links a:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.15);
            background: var(--verde-suave);
            color: white;
        }
        
        .screenshots {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
            margin: 2rem 0;
        }
        
        .screenshot-card {
            background: var(--bege-claro);
            border-radius: 15px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .screenshot-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 50px rgba(0,0,0,0.15);
        }
        
        .screenshot-card img {
            width: 100%;
            height: 300px;
            object-fit: cover;
            display: block;
            border-bottom: 3px solid var(--verde-suave);
        }
        
        .screenshot-caption {
            padding: 1.5rem;
            text-align: center;
            font-weight: 600;
            color: var(--marrom-escuro);
            margin: 0;
        }
        
        footer {
            background: var(--marrom-escuro);
            color: var(--bege-claro);
            text-align: center;
            padding: 2rem;
        }
        
        footer p {
            margin: 0;
            text-align: center;
        }
        
        @media (max-width: 768px) {
            body {
                padding: 1rem;
            }
            
            h1 {
                font-size: 2.5rem;
            }
            
            h2 {
                font-size: 2rem;
            }
            
            .content {
                padding: 2rem 1.5rem;
            }
            
            header {
                padding: 3rem 2rem;
            }
            
            .feature-grid {
                grid-template-columns: 1fr;
            }
            
            .social-links {
                flex-direction: column;
            }
            
            .screenshots {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>☕ Café Literário Nelly</h1>
            <p class="subtitle">Onde o tempo para e as histórias começam</p>
            <div class="badges">
                <span class="badge">✅ Status: Concluído</span>
                <span class="badge">📱 Responsivo</span>
                <span class="badge">🎨 Design Moderno</span>
                <span class="badge">⚡ Performance</span>
            </div>
        </header>
        
        <div class="content">
            <h2>📖 Sobre o Projeto</h2>
            <p>
                O <strong>Café Literário Nelly</strong> é um website elegante e acolhedor desenvolvido para uma cafeteria que une o prazer do café com o amor pela leitura. O projeto apresenta uma experiência visual imersiva com design responsivo, animações suaves e uma paleta de cores inspirada em ambientes literários clássicos.
            </p>
            
            <h2>📸 Prévia do Projeto</h2>
            <div class="screenshots">
                <div class="screenshot-card">
                    <img src="./img/inicio.png" alt="Seção Hero do Café Literário Nelly">
                    <p class="screenshot-caption">Página Inicial - Hero Section</p>
                </div>
                <div class="screenshot-card">
                    <img src="./img/sobre.png" alt="Cardápio do Café Literário Nelly">
                    <p class="screenshot-caption">Cardápio Completo</p>
                </div>
                <div class="screenshot-card">
                    <img src="./img/cardapio.png" alt="Versão Mobile do Café Literário Nelly">
                    <p class="screenshot-caption">Versão Mobile Responsiva</p>
                </div>
            </div>
            
            <h2>✨ Características Principais</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="icon">🎨</div>
                    <h3>Design Sofisticado</h3>
                    <p>Paleta de cores em tons terrosos inspirados em cafeterias clássicas</p>
                </div>
                <div class="feature-card">
                    <div class="icon">📱</div>
                    <h3>Responsivo</h3>
                    <p>Adaptado para todos os dispositivos e tamanhos de tela</p>
                </div>
                <div class="feature-card">
                    <div class="icon">🎭</div>
                    <h3>Animações</h3>
                    <p>Transições suaves e efeitos de scroll elegantes</p>
                </div>
                <div class="feature-card">
                    <div class="icon">📍</div>
                    <h3>Localização</h3>
                    <p>Integração com Google Maps para fácil localização</p>
                </div>
            </div>
            
            <h2>🛠️ Tecnologias Utilizadas</h2>
            <table class="tech-table">
                <thead>
                    <tr>
                        <th>Tecnologia</th>
                        <th>Descrição</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td><strong>HTML5</strong></td>
                        <td>Estrutura e marcação semântica do documento</td>
                    </tr>
                    <tr>
                        <td><strong>CSS3</strong></td>
                        <td>Estilização avançada, animações e responsividade</td>
                    </tr>
                    <tr>
                        <td><strong>JavaScript</strong></td>
                        <td>Interatividade, menu hambúrguer e animações de scroll</td>
                    </tr>
                    <tr>
                        <td><strong>Google Fonts</strong></td>
                        <td>Tipografias Crimson Text e Montserrat</td>
                    </tr>
                    <tr>
                        <td><strong>Google Maps API</strong></td>
                        <td>Integração de mapa para localização</td>
                    </tr>
                </tbody>
            </table>
            
            <h2>🚀 Como Executar o Projeto</h2>
            <h3>1. Clone o repositório</h3>
            <div class="code-block">git clone https://github.com/danielly-pedrini/cafe-literario-nelly.git<br>cd cafe-literario-nelly</div>
            
            <h3>2. Estrutura de arquivos</h3>
            <div class="code-block">cafe-literario-nelly/<br>│<br>├── index.html<br>├── styles.css<br>├── img/<br>│   ├── logo.png<br>│   └── cafe-literario.png<br>└── README.md</div>
            
            <h3>3. Execute o projeto</h3>
            <p>Abra o arquivo <strong>index.html</strong> no seu navegador favorito ou use uma extensão como Live Server no VS Code.</p>
            
            <h2>🎨 Paleta de Cores</h2>
            <div class="color-palette">
                <div class="color-box">
                    <div class="color-sample" style="background: #EAE0D5;"></div>
                    <div class="color-info">
                        <strong>Bege Claro</strong><br>#EAE0D5
                    </div>
                </div>
                <div class="color-box">
                    <div class="color-sample" style="background: #D4C5B9;"></div>
                    <div class="color-info">
                        <strong>Bege</strong><br>#D4C5B9
                    </div>
                </div>
                <div class="color-box">
                    <div class="color-sample" style="background: #4A3F35;"></div>
                    <div class="color-info">
                        <strong>Marrom</strong><br>#4A3F35
                    </div>
                </div>
                <div class="color-box">
                    <div class="color-sample" style="background: #2C2218;"></div>
                    <div class="color-info">
                        <strong>Marrom Escuro</strong><br>#2C2218
                    </div>
                </div>
                <div class="color-box">
                    <div class="color-sample" style="background: #8B9D83;"></div>
                    <div class="color-info">
                        <strong>Verde Suave</strong><br>#8B9D83
                    </div>
                </div>
                <div class="color-box">
                    <div class="color-sample" style="background: #F5F1E8;"></div>
                    <div class="color-info">
                        <strong>Creme</strong><br>#F5F1E8
                    </div>
                </div>
            </div>
            
            <h2>🎯 Funcionalidades</h2>
            <ul class="checklist">
                <li>Header fixo com navegação suave entre seções</li>
                <li>Seção Hero com animações flutuantes</li>
                <li>Página "Sobre" com texto acolhedor e elegante</li>
                <li>Cardápio completo organizado por 6 categorias</li>
                <li>Sistema de preços por tamanho (P/M/G) para bebidas</li>
                <li>Footer com informações de contato completas</li>
                <li>Mapa interativo do Google Maps</li>
                <li>Animações de entrada ao fazer scroll</li>
                <li>Menu hambúrguer responsivo para mobile</li>
            </ul>
            
            <h2>📱 Responsividade</h2>
            <p>O site é totalmente responsivo com breakpoint em <strong>768px</strong>, incluindo:</p>
            <ul class="checklist">
                <li>Menu hambúrguer animado para dispositivos móveis</li>
                <li>Layout em coluna única no mobile</li>
                <li>Tamanhos de fonte adaptados</li>
                <li>Imagens redimensionadas automaticamente</li>
            </ul>
            
            <h2>🗂️ Categorias do Cardápio</h2>
            <div class="feature-grid">
                <div class="feature-card">
                    <div class="icon">☕</div>
                    <p><strong>Cafés Tradicionais</strong></p>
                </div>
                <div class="feature-card">
                    <div class="icon">🍫</div>
                    <p><strong>Bebidas Especiais</strong></p>
                </div>
                <div class="feature-card">
                    <div class="icon">🧁</div>
                    <p><strong>Bolos & Doces</strong></p>
                </div>
                <div class="feature-card">
                    <div class="icon">🥐</div>
                    <p><strong>Salgados</strong></p>
                </div>
                <div class="feature-card">
                    <div class="icon">🥤</div>
                    <p><strong>Bebidas Frias</strong></p>
                </div>
                <div class="feature-card">
                    <div class="icon">🌿</div>
                    <p><strong>Especiais da Casa</strong></p>
                </div>
            </div>
            
            <h2>🌟 Melhorias Futuras</h2>
            <ul class="checklist future">
                <li>Sistema de reservas online</li>
                <li>Galeria de fotos do café</li>
                <li>Blog com artigos sobre café e literatura</li>
                <li>Integração com redes sociais</li>
                <li>Newsletter para clientes</li>
                <li>Sistema de avaliações</li>
                <li>Modo escuro (Dark mode)</li>
                <li>Internacionalização (i18n)</li>
            </ul>
            
            <div class="contact-info">
                <h3>📧 Contato do Estabelecimento</h3>
                <p>📍 Rua dos Livros, 123 - Centro, Porto Feliz - SP</p>
                <p>🕐 Segunda a Sábado: 8h às 20h | Domingo: 9h às 18h</p>
                <p>📞 (15) 3262-0000</p>
            </div>
            
            <div class="author-section">
                <h2>👩‍💻 Autora</h2>
                <h3>Danielly Pedrini</h3>
                <p>Desenvolvedora apaixonada por criar experiências web elegantes e funcionais</p>
                <div class="social-links">
                    <a href="https://github.com/danielly-pedrini" target="_blank">
                        🐙 GitHub
                    </a>
                    <a href="https://www.linkedin.com/in/daniellypedrini/" target="_blank">
                        💼 LinkedIn
                    </a>
                </div>
            </div>
        </div>
        
        <footer>
            <p>© 2025 Café Literário Nelly — Desenvolvido com ☕ e 📚 por Danielly Pedrini</p>
            <p style="margin-top: 1rem; opacity: 0.7;">⭐ Se este projeto te ajudou, considere dar uma estrela no GitHub!</p>
        </footer>
    </div>
</body>
</html>