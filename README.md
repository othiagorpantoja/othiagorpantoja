<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>README Interativo - Projeto Incrível</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #333;
            min-height: 100vh;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            padding: 60px 20px;
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.2);
            animation: fadeIn 1s ease-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: 700;
            color: white;
            margin-bottom: 20px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .header p {
            font-size: 1.2rem;
            color: rgba(255, 255, 255, 0.9);
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            padding: 30px 20px;
            border-radius: 15px;
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: #fff;
            display: block;
            margin-bottom: 10px;
        }

        .stat-label {
            color: rgba(255, 255, 255, 0.8);
            font-size: 1rem;
        }

        .section {
            background: white;
            margin: 30px 0;
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            animation: slideIn 0.6s ease-out forwards;
            opacity: 0;
            transform: translateY(30px);
        }

        @keyframes slideIn {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .section h2 {
            font-size: 2.2rem;
            margin-bottom: 20px;
            color: #2c3e50;
            border-bottom: 3px solid #667eea;
            padding-bottom: 10px;
            display: inline-block;
        }

        .features-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-top: 30px;
        }

        .feature-card {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 25px;
            border-radius: 15px;
            transition: all 0.3s ease;
            border-left: 5px solid #667eea;
        }

        .feature-card:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.2);
        }

        .feature-icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .code-block {
            background: #2d3748;
            color: #e2e8f0;
            padding: 20px;
            border-radius: 10px;
            font-family: 'Courier New', monospace;
            margin: 20px 0;
            position: relative;
            overflow-x: auto;
        }

        .copy-btn {
            position: absolute;
            top: 10px;
            right: 10px;
            background: #667eea;
            color: white;
            border: none;
            padding: 5px 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 0.8rem;
            transition: background 0.3s ease;
        }

        .copy-btn:hover {
            background: #5a6fd8;
        }

        .copy-btn.copied {
            background: #28a745;
        }

        .demo-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
            margin: 30px 0;
        }

        .demo-btn {
            background: linear-gradient(45deg, #667eea, #764ba2);
            color: white;
            border: none;
            padding: 15px 25px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 1rem;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(102, 126, 234, 0.3);
        }

        .demo-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(102, 126, 234, 0.4);
        }

        .demo-btn:active {
            transform: translateY(-1px);
        }

        .toggle-btn {
            background: #667eea;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 1rem;
            margin-bottom: 15px;
            transition: background 0.3s ease;
        }

        .toggle-btn:hover {
            background: #5a6fd8;
        }

        .toggle-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease;
            background: #f8f9fa;
            border-radius: 8px;
        }

        .toggle-content.active {
            max-height: 400px;
            padding: 20px;
            margin-bottom: 20px;
        }

        .notification {
            position: fixed;
            top: 20px;
            right: 20px;
            background: #28a745;
            color: white;
            padding: 15px 20px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transform: translateX(400px);
            transition: transform 0.3s ease;
            z-index: 1000;
        }

        .notification.show {
            transform: translateX(0);
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: #e9ecef;
            border-radius: 4px;
            overflow: hidden;
            margin: 20px 0;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(45deg, #667eea, #764ba2);
            width: 0%;
            transition: width 2s ease;
        }

        .theme-toggle {
            position: fixed;
            top: 20px;
            left: 20px;
            background: rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.3);
            color: white;
            padding: 10px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            z-index: 100;
        }

        .theme-toggle:hover {
            background: rgba(255, 255, 255, 0.3);
            transform: scale(1.1);
        }

        .dark-theme {
            background: linear-gradient(135deg, #2c3e50 0%, #34495e 100%);
        }

        .dark-theme .section {
            background: #34495e;
            color: white;
        }

        .dark-theme .section h2 {
            color: #ecf0f1;
        }

        .installation-step {
            background: #f8f9fa;
            padding: 20px;
            border-radius: 10px;
            margin: 15px 0;
            border-left: 4px solid #667eea;
            position: relative;
        }

        .step-number {
            position: absolute;
            left: -15px;
            top: 15px;
            background: #667eea;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
        }

        @media (max-width: 768px) {
            .header h1 { font-size: 2.5rem; }
            .container { padding: 15px; }
            .section { padding: 25px 20px; }
            .demo-buttons { flex-direction: column; align-items: center; }
            .features-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <button class="theme-toggle" onclick="toggleTheme()">🌓</button>
    
    <div class="notification" id="notification"></div>

    <div class="container">
        <header class="header">
            <h1>🚀 Projeto Incrível</h1>
            <p>Uma aplicação moderna e interativa que vai revolucionar sua experiência de desenvolvimento</p>
        </header>

        <div class="stats">
            <div class="stat-card" onclick="animateCounter(this)">
                <span class="stat-number">2,547</span>
                <span class="stat-label">Downloads</span>
            </div>
            <div class="stat-card" onclick="animateCounter(this)">
                <span class="stat-number">⭐ 1,234</span>
                <span class="stat-label">Stars GitHub</span>
            </div>
            <div class="stat-card" onclick="animateCounter(this)">
                <span class="stat-number">47</span>
                <span class="stat-label">Contribuidores</span>
            </div>
            <div class="stat-card" onclick="animateCounter(this)">
                <span class="stat-number">v2.1.0</span>
                <span class="stat-label">Versão Atual</span>
            </div>
        </div>

        <section class="section">
            <h2>📋 Sobre o Projeto</h2>
            <p>Este README interativo demonstra como criar documentação envolvente e funcional. O projeto combina design moderno com funcionalidades práticas para melhorar a experiência do desenvolvedor.</p>
            
            <div class="progress-bar">
                <div class="progress-fill" id="progressBar"></div>
            </div>
            
            <p><strong>Principais benefícios:</strong> Interface intuitiva, animações suaves, responsividade total e interatividade avançada.</p>
        </section>

        <section class="section">
            <h2>⚡ Funcionalidades</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="feature-icon">🎨</div>
                    <h3>Design Moderno</h3>
                    <p>Interface elegante com glassmorphism e gradientes suaves</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">📱</div>
                    <h3>Totalmente Responsivo</h3>
                    <p>Funciona perfeitamente em todos os dispositivos e tamanhos de tela</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">⚡</div>
                    <h3>Performance Otimizada</h3>
                    <p>Carregamento rápido e animações fluidas sem travamentos</p>
                </div>
                <div class="feature-card">
                    <div class="feature-icon">🔧</div>
                    <h3>Altamente Customizável</h3>
                    <p>Fácil de personalizar cores, textos e comportamentos</p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>🚀 Instalação Rápida</h2>
            
            <div class="installation-step">
                <div class="step-number">1</div>
                <h3>Clone o Repositório</h3>
                <div class="code-block">
                    <button class="copy-btn" onclick="copyToClipboard(this, 'git clone https://github.com/usuario/projeto-incrivel.git')">Copiar</button>
                    <code>git clone https://github.com/usuario/projeto-incrivel.git</code>
                </div>
            </div>

            <div class="installation-step">
                <div class="step-number">2</div>
                <h3>Instalar Dependências</h3>
                <div class="code-block">
                    <button class="copy-btn" onclick="copyToClipboard(this, 'npm install')">Copiar</button>
                    <code>npm install</code>
                </div>
            </div>

            <div class="installation-step">
                <div class="step-number">3</div>
                <h3>Executar Projeto</h3>
                <div class="code-block">
                    <button class="copy-btn" onclick="copyToClipboard(this, 'npm start')">Copiar</button>
                    <code>npm start</code>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>📚 Documentação</h2>
            
            <button class="toggle-btn" onclick="toggleSection('apiDocs')">
                📖 Documentação da API
            </button>
            <div class="toggle-content" id="apiDocs">
                <h3>Endpoints Principais</h3>
                <div class="code-block">
                    <button class="copy-btn" onclick="copyToClipboard(this, 'GET /api/users\nPOST /api/users\nPUT /api/users/:id\nDELETE /api/users/:id')">Copiar</button>
                    <code>GET /api/users      # Listar usuários<br>
POST /api/users     # Criar usuário<br>
PUT /api/users/:id  # Atualizar usuário<br>
DELETE /api/users/:id # Deletar usuário</code>
                </div>
            </div>

            <button class="toggle-btn" onclick="toggleSection('examples')">
                💡 Exemplos de Uso
            </button>
            <div class="toggle-content" id="examples">
                <div class="code-block">
                    <button class="copy-btn" onclick="copyToClipboard(this, 'const projeto = new ProjetoIncrivel({\n  theme: \"dark\",\n  animations: true\n});\n\nprojeto.init();')">Copiar</button>
                    <code>const projeto = new ProjetoIncrivel({<br>
&nbsp;&nbsp;theme: "dark",<br>
&nbsp;&nbsp;animations: true<br>
});<br><br>
projeto.init();</code>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>🎮 Demonstração Interativa</h2>
            <p>Teste as funcionalidades do projeto clicando nos botões abaixo:</p>
            
            <div class="demo-buttons">
                <button class="demo-btn" onclick="showNotification('🎉 Funcionalidade 1 ativada com sucesso!')">
                    Testar Funcionalidade 1
                </button>
                <button class="demo-btn" onclick="animateCards()">
                    🎨 Animar Cards
                </button>
                <button class="demo-btn" onclick="showRandomTip()">
                    💡 Dica Aleatória
                </button>
                <button class="demo-btn" onclick="simulateProgress()">
                    📊 Simular Progresso
                </button>
            </div>
        </section>

        <section class="section">
            <h2>🤝 Como Contribuir</h2>
            <p>Adoramos contribuições! Siga estes passos simples:</p>
            <ol style="margin: 20px 0; padding-left: 20px;">
                <li>Faça um fork do projeto</li>
                <li>Crie uma branch para sua feature (<code>git checkout -b feature/MinhaFeature</code>)</li>
                <li>Commit suas mudanças (<code>git commit -m 'Adiciona MinhaFeature'</code>)</li>
                <li>Push para a branch (<code>git push origin feature/MinhaFeature</code>)</li>
                <li>Abra um Pull Request</li>
            </ol>
        </section>

        <section class="section">
            <h2>📧 Contato</h2>
            <p>Entre em contato conosco através dos canais abaixo:</p>
            <div class="demo-buttons">
                <button class="demo-btn" onclick="showNotification('🐙 Visite nosso GitHub!')">
                    GitHub
                </button>
                <button class="demo-btn" onclick="showNotification('💬 Em breve teremos Discord!')">
                    Discord
                </button>
                <button class="demo-btn" onclick="showNotification('📧 Email: contato@projeto.com')">
                    Email
                </button>
            </div>
        </section>
    </div>

    <script>
        // Animar seções ao carregar
        document.addEventListener('DOMContentLoaded', function() {
            const sections = document.querySelectorAll('.section');
            sections.forEach((section, index) => {
                section.style.animationDelay = `${index * 0.2}s`;
            });
            
            // Animar barra de progresso
            setTimeout(() => {
                document.getElementById('progressBar').style.width = '75%';
            }, 1500);
        });

        // Função para mostrar notificação
        function showNotification(message) {
            const notification = document.getElementById('notification');
            notification.textContent = message;
            notification.classList.add('show');
            
            setTimeout(() => {
                notification.classList.remove('show');
            }, 3000);
        }

        // Função para copiar texto
        function copyToClipboard(button, text) {
            navigator.clipboard.writeText(text).then(() => {
                button.textContent = 'Copiado!';
                button.classList.add('copied');
                
                setTimeout(() => {
                    button.textContent = 'Copiar';
                    button.classList.remove('copied');
                }, 2000);
                
                showNotification('📋 Código copiado para a área de transferência!');
            });
        }

        // Função para alternar seções
        function toggleSection(sectionId) {
            const section = document.getElementById(sectionId);
            section.classList.toggle('active');
        }

        // Função para alternar tema
        function toggleTheme() {
            document.body.classList.toggle('dark-theme');
            const isDark = document.body.classList.contains('dark-theme');
            showNotification(isDark ? '🌙 Tema escuro ativado!' : '☀️ Tema claro ativado!');
        }

        // Função para animar cards
        function animateCards() {
            const cards = document.querySelectorAll('.feature-card');
            cards.forEach((card, index) => {
                setTimeout(() => {
                    card.style.transform = 'scale(1.1) rotate(2deg)';
                    setTimeout(() => {
                        card.style.transform = 'scale(1) rotate(0deg)';
                    }, 300);
                }, index * 100);
            });
            showNotification('🎨 Cards animados!');
        }

        // Função para mostrar dica aleatória
        function showRandomTip() {
            const tips = [
                '💡 Dica: Use Ctrl+C para copiar códigos rapidamente!',
                '🎯 Dica: Teste o modo escuro clicando no botão superior esquerdo!',
                '⚡ Dica: Todos os elementos são responsivos e se adaptam ao seu dispositivo!',
                '🚀 Dica: Este README foi criado com HTML, CSS e JavaScript puro!'
            ];
            const randomTip = tips[Math.floor(Math.random() * tips.length)];
            showNotification(randomTip);
        }

        // Função para simular progresso
        function simulateProgress() {
            const progressBar = document.getElementById('progressBar');
            const randomProgress = Math.floor(Math.random() * 100) + 1;
            progressBar.style.width = randomProgress + '%';
            showNotification(`📊 Progresso simulado: ${randomProgress}%`);
        }

        // Função para animar contador
        function animateCounter(card) {
            const numberElement = card.querySelector('.stat-number');
            const originalText = numberElement.textContent;
            
            let count = 0;
            const target = Math.floor(Math.random() * 1000) + 500;
            const increment = target / 30;
            
            const timer = setInterval(() => {
                count += increment;
                if (count >= target) {
                    count = target;
                    clearInterval(timer);
                    setTimeout(() => {
                        numberElement.textContent = originalText;
                    }, 2000);
                }
                numberElement.textContent = Math.floor(count).toLocaleString();
            }, 50);
            
            showNotification('🔢 Contador animado!');
        }
    </script>
</body>
</html>
