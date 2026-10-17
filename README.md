<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desenvolvimento de Sistemas - O Seu Futuro Começa Aqui!</title>
    <style>
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --accent: #ec4899;
            --accent-green: #10b981;
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-color: #f8fafc;
            --text-muted: #94a3b8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 50px 20px;
            background: linear-gradient(135deg, rgba(99, 102, 241, 0.15) 0%, rgba(236, 72, 153, 0.15) 100%);
            border-radius: 16px;
            margin-bottom: 40px;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }

        .hero h1 {
            font-size: 2.8rem;
            color: var(--text-color);
            margin-bottom: 15px;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero p {
            font-size: 1.2rem;
            color: #cbd5e1;
            max-width: 700px;
            margin: 0 auto 25px auto;
        }

        .cta-btn-header {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            text-decoration: none;
            padding: 14px 28px;
            font-weight: bold;
            border-radius: 30px;
            font-size: 1.1rem;
            transition: transform 0.2s, background 0.3s;
        }

        .cta-btn-header:hover {
            transform: scale(1.05);
            background-color: #db2777;
        }

        /* Seções de Conteúdo */
        .section-card {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 35px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.3);
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .section-title {
            font-size: 1.8rem;
            color: var(--primary);
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        /* Por que escolher DS? */
        .benefits-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .benefit-item {
            background: rgba(255, 255, 255, 0.03);
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid var(--accent-green);
        }

        .benefit-item h4 {
            color: var(--accent-green);
            font-size: 1.1rem;
            margin-bottom: 8px;
        }

        /* História do DS */
        .history-card {
            border-left: 4px solid var(--accent);
        }

        .pioneer-box {
            background: rgba(236, 72, 153, 0.08);
            border-radius: 10px;
            padding: 20px;
            margin-top: 20px;
        }

        .pioneer-box h4 {
            color: var(--accent);
            font-size: 1.2rem;
            margin-bottom: 8px;
        }

        /* Indução ao Quiz */
        .quiz-intro {
            text-align: center;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            padding: 30px;
            border-radius: 12px;
            margin-bottom: 30px;
        }

        .quiz-intro h2 {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        /* Quiz Container */
        .question-box {
            margin-bottom: 25px;
            background: rgba(255, 255, 255, 0.02);
            padding: 20px;
            border-radius: 10px;
        }

        .question-box h3 {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #e2e8f0;
        }

        .options {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .option-label {
            background: rgba(255, 255, 255, 0.05);
            padding: 14px 18px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid transparent;
            font-size: 1rem;
        }

        .option-label:hover {
            background: rgba(99, 102, 241, 0.15);
            border-color: var(--primary);
        }

        .option-label input {
            margin-right: 12px;
            transform: scale(1.2);
        }

        button.submit-btn {
            background: linear-gradient(90deg, var(--accent) 0%, var(--primary) 100%);
            color: white;
            border: none;
            padding: 16px 30px;
            font-size: 1.2rem;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            transition: opacity 0.3s, transform 0.2s;
            margin-top: 10px;
        }

        button.submit-btn:hover {
            opacity: 0.9;
            transform: translateY(-2px);
        }

        /* Resultado */
        .result-box {
            display: none;
            text-align: center;
            padding: 30px;
            background: var(--card-bg);
            border-radius: 12px;
            border: 2px solid var(--accent-green);
        }

        .result-box h2 {
            color: var(--accent-green);
            font-size: 2.2rem;
            margin-bottom: 15px;
        }

        .result-box p {
            font-size: 1.2rem;
            color: #cbd5e1;
            margin-bottom: 25px;
        }
    </style>
</head>
<body>

    <div class="container">
        <!-- Banner Principal -->
        <header class="hero">
            <h1>Desenvolvimento de <span>Sistemas</span></h1>
            <p>Mais do que aprender a programar: o curso onde você aprende a criar o futuro, resolver problemas reais e construir suas próprias ideias!</p>
            <a href="#quiz-anchor" class="cta-btn-header">Descubra se o curso é para você ↓</a>
        </header>

        <!-- Seção 1: Por que escolher DS? -->
        <section class="section-card">
            <h2 class="section-title">🚀 Por que escolher o Curso Técnico em DS?</h2>
            <p>Se você usa celular, joga games, acessa redes sociais ou compra online, você já consome o que os desenvolvedores criam. Mas no curso de DS, você passa do lado de quem apenas usa para o lado de <strong>quem cria</strong>!</p>
            
            <div class="benefits-grid">
                <div class="benefit-item">
                    <h4>💡 Crie seus próprios Projetos</h4>
                    <p>Aprenda a criar aplicativos, sites, sistemas e até lógica para games do zero absoluto.</p>
                </div>
                <div class="benefit-item">
                    <h4>📈 Mercado em Alta Explosiva</h4>
                    <p>Tecnologia é a área que mais contrata no mundo, com altíssimos salários e possibilidade de trabalhar até de casa.</p>
                </div>
                <div class="benefit-item">
                    <h4>🧠 Desenvolva seu Raciocínio</h4>
                    <p>Aprenda a pensar como um resolvedor de problemas profissional. Uma habilidade que serve para qualquer profissão no futuro.</p>
                </div>
            </div>
        </section>

        <!-- Seção 2: A História de DS e as Mulheres que Mudaram Tudo -->
        <section class="section-card history-card">
            <h2 class="section-title">📜 A História de DS e o Protagonismo Feminino</h2>
            <p>A história da computação não começou em garagens com garotos nerds. Ela começou com **mulheres revolucionárias** que inventaram os conceitos que usamos até hoje!</p>

            <div class="pioneer-box">
                <h4>👩‍💻 Ada Lovelace (1840) — A Primeira Programadora do Mundo</h4>
                <p>Antes mesmo de existir o primeiro computador elétrico, Ada escreveu o primeiro algoritmo da história da humanidade. Ela enxergou que as máquinas poderiam processar mais do que números: poderiam criar música, arte e sistemas!</p>
            </div>

            <div class="pioneer-box">
                <h4>🚀 Margaret Hamilton (1969) — Salvação da Apollo 11</h4>
                <p>Quando a nave da NASA estava prestes a pousar na Lua, o computador quase travou por sobrecarga. O código desenvolvido pela equipe de Margaret Hamilton priorizou as tarefas vitais e salvou o Pouso na Lua! Ela inclusive criou o termo <em>"Engenharia de Software"</em>.</p>
            </div>

            <p style="margin-top: 20px; font-weight: bold; color: #e2e8f0;">
                ⚡ Preconceito não combina com Tecnologia: Programação, exatas e lógica não têm gênero. DS é para qualquer pessoa que queira inovar e transformar o mundo!
            </p>
        </section>

        <!-- Chamada para Induzir ao Quiz -->
        <div class="quiz-intro" id="quiz-anchor">
            <h2>Pronto para descobrir o seu potencial?</h2>
            <p>Responda ao nosso Quiz Rápido e veja o quanto o seu perfil combina com o curso de Desenvolvimento de Sistemas!</p>
        </div>

        <!-- Seção 3: Quiz Interativo -->
        <div class="section-card" id="quiz-card">
            <form id="dsQuiz">
                
                <div class="question-box">
                    <h3>1. Quando você tá jogando ou usando um app e ele dá um bug bizarro, qual é seu impulso?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q1" value="1"> Passar raiva, fechar o app e ir fazer outra coisa.</label>
                        <label class="option-label"><input type="radio" name="q1" value="2"> Acho chato, mas espero voltar a funcionar.</label>
                        <label class="option-label"><input type="radio" name="q1" value="3" required> Fico curioso tentando entender por que deu ruim e tento testar de novo!</label>
                    </div>
                </div>

                <div class="question-box">
                    <h3>2. Se você pudesse ter um "superpoder digital" hoje, qual escolheria?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q2" value="1"> Ter acesso a todos os jogos e apps do mundo de graça.</label>
                        <label class="option-label"><input type="radio" name="q2" value="2"> Saber personalizar e configurar todo o meu celular/PC ao máximo.</label>
                        <label class="option-label"><input type="radio" name="q2" value="3" required> Criar o meu próprio jogo, aplicativo ou site do zero!</label>
                    </div>
                </div>

                <div class="question-box">
                    <h3>3. Como sua mente reage diante de uma tarefa chata e repetitiva no dia a dia?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q3" value="1"> Faço logo rezando para acabar rápido.</label>
                        <label class="option-label"><input type="radio" name="q3" value="2"> Deixo para fazer no último minuto.</label>
                        <label class="option-label"><input type="radio" name="q3" value="3" required> Penso: "Com certeza dá para criar uma automação/robô para fazer isso em 2 segundos."</label>
                    </div>
                </div>

                <div class="question-box">
                    <h3>4. Quando você descobre como funcionam os algoritmos de recomendação (tipo TikTok ou Instagram):</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q4" value="1"> Nem ligo, só quero rolar o feed.</label>
                        <label class="option-label"><input type="radio" name="q4" value="2"> Acho curioso, mas sigo usando normal.</label>
                        <label class="option-label"><input type="radio" name="q4" value="3" required> Acho fascinante! Queria ver a lógica por trás disso para entender o código.</label>
                    </div>
                </div>

                <div class="question-box">
                    <h3>5. Se falta só UMA peça ou um detalhe para o seu projeto funcionar, você:</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q5" value="1"> Largo mão, desisto fácil.</label>
                        <label class="option-label"><input type="radio" name="q5" value="2"> Peço para outra pessoa tentar resolver.</label>
                        <label class="option-label"><input type="radio" name="q5" value="3" required> Fico obstinado! Não me deito sossegado enquanto não achar o erro e fazer funcionar.</label>
                    </div>
                </div>

                <button type="button" class="submit-btn" onclick="calcularResultado()">Ver Meu Resultado no Quiz</button>
            </form>
        </div>

        <!-- Tela de Resultado do Quiz -->
        <div class="result-box" id="result-card">
            <h2 id="result-title"></h2>
            <p id="result-text"></p>
            <button class="submit-btn" onclick="reiniciarQuiz()">Refazer o Quiz</button>
        </div>
    </div>

    <script>
        function calcularResultado() {
            const q1 = document.querySelector('input[name="q1"]:checked');
            const q2 = document.querySelector('input[name="q2"]:checked');
            const q3 = document.querySelector('input[name="q3"]:checked');
            const q4 = document.querySelector('input[name="q4"]:checked');
            const q5 = document.querySelector('input[name="q5"]:checked');

            if (!q1 || !q2 || !q3 || !q4 || !q5) {
                alert("Por favor, responda a todas as perguntas antes de ver seu resultado!");
                return;
            }

            let soma = parseInt(q1.value) + parseInt(q2.value) + parseInt(q3.value) + parseInt(q4.value) + parseInt(q5.value);

            let titulo = "";
            let mensagem = "";

            if (soma >= 12) {
                titulo = "🚀 Perfil Dev Confirmado!";
                mensagem = "Sua mente é curiosa, lógica e focada em resolver desafios. Você tem exatamente o perfil que o curso de Desenvolvimento de Sistemas precisa. Venha fazer parte do curso!";
            } else if (soma >= 8) {
                titulo = "💡 Grande Potencial Explorador!";
                mensagem = "Você tem excelente afinidade com inovação e resolução de problemas. No curso de DS, você vai aprender a transformar essa curiosidade em projetos incríveis de verdade!";
            } else {
                titulo = "🎨 Potencial para Inovação!";
                mensagem = "Mesmo que você goste de outras áreas, aprender lógica e tecnologia em DS vai te colocar passos à frente em qualquer profissão do futuro. Vale a pena experimentar!";
            }

            document.getElementById("quiz-card").style.display = "none";
            document.getElementById("result-card").style.display = "block";
            document.getElementById("result-title").innerText = titulo;
            document.getElementById("result-text").innerText = mensagem;
        }

        function reiniciarQuiz() {
            document.getElementById("dsQuiz").reset();
            document.getElementById("result-card").style.display = "none";
            document.getElementById("quiz-card").style.display = "block";
        }
    </script>
</body>
</html>
