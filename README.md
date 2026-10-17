<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desenvolvimento de Sistemas - Seu Futuro Começa Aqui!</title>
    <style>
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --accent: #ec4899;
            --accent-green: #10b981;
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-color: #f8fafc;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Segoe UI', Roboto, sans-serif; }
        body { background-color: var(--bg-color); color: var(--text-color); line-height: 1.6; }
        .container { max-width: 900px; margin: 0 auto; padding: 20px; }

        /* Hero chamativo */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.2) 0%, rgba(236, 72, 153, 0.2) 100%);
            border-radius: 20px;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .hero h1 { font-size: 3rem; margin-bottom: 15px; }
        .hero h1 span { color: var(--accent); }
        .hero p { font-size: 1.25rem; color: #cbd5e1; max-width: 700px; margin: 0 auto 30px auto; }

        .section-card {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 35px;
            margin-bottom: 35px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.3);
        }

        .section-card h2 { font-size: 1.8rem; color: var(--primary); margin-bottom: 15px; }

        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .benefit-item {
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 12px;
            border-left: 4px solid var(--accent-green);
        }

        .benefit-item h3 { color: var(--accent-green); margin-bottom: 8px; font-size: 1.2rem; }

        /* Seção de Botões de Redirecionamento */
        .actions-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }

        .action-card {
            background: linear-gradient(145deg, rgba(30, 41, 59, 0.9), rgba(15, 23, 42, 0.9));
            border: 2px solid rgba(255, 255, 255, 0.1);
            border-radius: 16px;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s, border-color 0.3s;
        }

        .action-card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .action-card.quiz-card { border-color: var(--accent); }
        .action-card.quiz-card:hover { border-color: #db2777; }

        .action-card h3 { font-size: 1.5rem; margin-bottom: 10px; }
        .action-card p { color: #94a3b8; margin-bottom: 20px; font-size: 1rem; }

        .btn {
            display: inline-block;
            width: 100%;
            padding: 14px 20px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            transition: background 0.3s;
        }

        .btn-quiz { background-color: var(--accent); color: white; }
        .btn-quiz:hover { background-color: #db2777; }

        .btn-history { background-color: var(--primary); color: white; }
        .btn-history:hover { background-color: var(--primary-dark); }
    </style>
</head>
<body>

    <div class="container">
        <!-- Banner Principal Chamativo -->
        <header class="hero">
            <h1>Desenvolvimento de <span>Sistemas</span></h1>
            <p>Deixe de ser apenas um usuário de aplicativos e jogos. Aprenda a criar o seu próprio futuro, desenvolver sistemas reais e dominar a profissão mais requisitada do mundo!</p>
        </header>

        <!-- Por que fazer DS? -->
        <section class="section-card">
            <h2>🔥 Por que você DEVE fazer o Curso Técnico de DS?</h2>
            <p>O curso técnico em Desenvolvimento de Sistemas prepara você para o mercado antes mesmo de sair do colégio. Não importa a sua área de interesse futura, aprender a programar vai te colocar anos-luz à frente!</p>

            <div class="benefits-grid">
                <div class="benefit-item">
                    <h3>💡 De Consumidor a Criador</h3>
                    <p>Aprenda a construir sites, aplicativos para celular, automações e sistemas para web do zero!</p>
                </div>
                <div class="benefit-item">
                    <h3>🚀 O Mercado que Mais Contrata</h3>
                    <p>Tecnologia tem vagas sobrando e oferece ótimos salários com possibilidade de trabalhar de onde quiser.</p>
                </div>
                <div class="benefit-item">
                    <h3>🧠 Raciocínio & Resolução</h3>
                    <p>Aprenda a pensar de forma lógica, rápida e estruturada. Uma habilidade valorizada em qualquer carreira.</p>
                </div>
            </div>
        </section>

        <!-- Opções de Redirecionamento -->
        <div class="actions-container">
            <div class="action-card quiz-card">
                <h3>🎮 Quiz de Perfil</h3>
                <p>Será que o curso de DS combina com você? Responda a 5 perguntas rápidas e descubra agora!</p>
                <a href="quiz.html" class="btn btn-quiz">Fazer o Quiz Agora →</a>
            </div>

            <div class="action-card">
                <h3>📜 Saiba Mais & História</h3>
                <p>Descubra como a programação nasceu, conheça as mulheres que revolucionaram a TI e veja mais detalhes do curso.</p>
                <a href="historia.html" class="btn btn-history">Conhecer a História →</a>
            </div>
        </div>
    </div>

</body>
</html>
