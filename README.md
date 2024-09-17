<html><head><base href=""><meta charset="UTF-8"><meta name="viewport" content="width=device-width, initial-scale=1.0"><title>Investigador Místico: Elite Hacker Squad</title><style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&family=Rajdhani:wght@300;400;700&display=swap');

:root {
  --primary-color: #0a0e17;
  --secondary-color: #1a2130;
  --highlight-color: #00ffff;
  --accent-color: #ff00ff;
  --light-text: #e0e0e0;
  --font-primary: 'Rajdhani', sans-serif;
  --font-secondary: 'Orbitron', sans-serif;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body, html {
  height: 100%;
  font-family: var(--font-primary);
  background: var(--primary-color);
  color: var(--light-text);
  line-height: 1.6;
  overflow-x: hidden;
}

.cyber-grid {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    linear-gradient(to right, rgba(0,255,255,0.05) 1px, transparent 1px),
    linear-gradient(to bottom, rgba(0,255,255,0.05) 1px, transparent 1px);
  background-size: 20px 20px;
  z-index: -1;
  animation: gridPulse 15s infinite linear;
}

@keyframes gridPulse {
  0%, 100% { opacity: 0.2; }
  50% { opacity: 0.8; }
}

header {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px 0;
  text-align: center;
  position: relative;
  backdrop-filter: blur(10px);
}

header::before {
  content: "";
  position: absolute;
  top: -50%;
  left: -50%;
  width: 200%;
  height: 200%;
  background: radial-gradient(circle, rgba(0,255,255,0.1) 0%, rgba(0,255,255,0) 70%);
  animation: pulse 4s infinite alternate;
}

@keyframes pulse {
  0% { transform: scale(0.8); opacity: 0.5; }
  50% { transform: scale(1.2); opacity: 1; }
  100% { transform: scale(0.8); opacity: 0.5; }
}

header h1 {
  font-size: 3.5rem;
  margin: 0;
  font-family: var(--font-secondary);
  color: var(--highlight-color);
  text-shadow: 0 0 10px var(--highlight-color), 0 0 20px var(--highlight-color);
}

header p {
  font-size: 1.2rem;
  margin: 10px 0 0;
  color: var(--accent-color);
}

nav {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  flex-wrap: wrap;
}

nav a {
  margin: 10px 15px;
  color: var(--light-text);
  text-decoration: none;
  font-size: 1.1rem;
  position: relative;
  overflow: hidden;
  transition: color 0.3s ease;
}

nav a::before {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: var(--highlight-color);
  transform: translateX(-100%);
  transition: transform 0.3s ease;
}

nav a:hover::before {
  transform: translateX(0);
}

nav a:hover {
  color: var(--highlight-color);
  text-shadow: 0 0 5px var(--highlight-color);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 40px 20px;
}

section {
  margin: 60px 0;
  text-align: center;
  position: relative;
}

section::before {
  content: '';
  position: absolute;
  top: -20px;
  left: 50%;
  transform: translateX(-50%);
  width: 50px;
  height: 4px;
  background: var(--highlight-color);
  box-shadow: 0 0 10px var(--highlight-color);
}

section h2 {
  font-size: 2.5rem;
  color: var(--highlight-color);
  margin: 0 0 20px;
  font-family: var(--font-secondary);
  text-transform: uppercase;
  text-shadow: 0 0 10px var(--highlight-color);
}

section p {
  font-size: 1.1rem;
  line-height: 1.8;
  max-width: 800px;
  margin: 0 auto;
}

.tools-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 30px;
  margin-top: 40px;
}

.tool-card {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px;
  border-radius: 10px;
  position: relative;
  overflow: hidden;
  transition: all 0.3s;
  backdrop-filter: blur(5px);
}

.tool-card:hover {
  transform: translateY(-5px) scale(1.05);
  box-shadow: 0 5px 15px rgba(0,255,255,0.3);
}

.tool-card::before {
  content: '';
  position: absolute;
  top: -2px;
  left: -2px;
  right: -2px;
  bottom: -2px;
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  z-index: -1;
  filter: blur(10px);
  opacity: 0;
  transition: opacity 0.3s;
}

.tool-card:hover::before {
  opacity: 1;
}

.tool-card h3 {
  color: var(--highlight-color);
  font-family: var(--font-secondary);
  font-size: 1.5rem;
}

.tool-card p {
  font-size: 1rem;
  color: var(--light-text);
}

.team-members {
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  margin-top: 40px;
}

.team-member {
  flex-basis: calc(25% - 20px);
  margin-bottom: 30px;
  text-align: center;
}

.team-member img {
  width: 150px;
  height: 150px;
  border-radius: 50%;
  border: 3px solid var(--highlight-color);
  transition: all 0.3s;
  box-shadow: 0 0 15px var(--highlight-color);
}

.team-member:hover img {
  transform: scale(1.1) rotate(5deg);
  box-shadow: 0 0 30px var(--highlight-color);
}

.team-member h3 {
  margin-top: 15px;
  color: var(--highlight-color);
  font-family: var(--font-secondary);
}

.team-member p {
  font-size: 0.9rem;
  color: var(--accent-color);
}

.cta {
  background: rgba(26, 33, 48, 0.8);
  padding: 60px 0;
  text-align: center;
  position: relative;
  overflow: hidden;
  backdrop-filter: blur(10px);
}

.cta a {
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  color: var(--primary-color);
  padding: 15px 30px;
  border: none;
  text-transform: uppercase;
  font-weight: bold;
  font-size: 1.2rem;
  cursor: pointer;
  text-decoration: none;
  display: inline-block;
  border-radius: 5px;
  position: relative;
  transition: all 0.3s;
}

.cta a:hover {
  box-shadow: 0 5px 15px rgba(0,255,255,0.3);
  transform: translateY(-3px) scale(1.05);
}

footer {
  background: rgba(26, 33, 48, 0.8);
  padding: 20px;
  text-align: center;
  backdrop-filter: blur(10px);
}

footer p {
  margin: 0;
  font-size: 0.9rem;
  color: var(--accent-color);
}

#inscricao-modal {
  display: none;
  position: fixed;
  z-index: 1000;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.8);
  backdrop-filter: blur(5px);
}

.modal-content {
  background: var(--secondary-color);
  margin: 10% auto;
  padding: 20px;
  border: 1px solid var(--highlight-color);
  width: 80%;
  max-width: 600px;
  border-radius: 10px;
  box-shadow: 0 0 20px var(--highlight-color);
}

.close {
  color: var(--accent-color);
  float: right;
  font-size: 28px;
  font-weight: bold;
  cursor: pointer;
}

.close:hover {
  color: var(--highlight-color);
}

form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

form input, form textarea {
  padding: 10px;
  border: 1px solid var(--highlight-color);
  background: rgba(10, 14, 23, 0.8);
  color: var(--light-text);
  border-radius: 5px;
}

form button {
  background: linear-gradient(45deg, var(--highlight-color), var(--accent-color));
  color: var(--primary-color);
  padding: 10px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  border-radius: 5px;
  transition: all 0.3s;
}

form button:hover {
  transform: translateY(-2px);
  box-shadow: 0 5px 10px rgba(0,255,255,0.2);
}

@media (max-width: 768px) {
  .team-member {
    flex-basis: calc(50% - 20px);
  }

  header h1 {
    font-size: 2.5rem;
  }

  section h2 {
    font-size: 2rem;
  }
}

@media (max-width: 480px) {
  .team-member {
    flex-basis: 100%;
  }

  header h1 {
    font-size: 2rem;
  }

  section h2 {
    font-size: 1.75rem;
  }
}
</style>
</head>
<body>

<div class="cyber-grid"></div>

<header>
  <h1>Investigador Místico</h1>
  <p>Elite Hacker Squad</p>
</header>

<nav>
  <a href="#">Início</a>
  <a href="#">Ferramentas</a>
  <a href="#">Equipe</a>
  <a href="#">Contato</a>
</nav>

<div class="container">
  <section>
    <h2>Bem-vindo ao Futuro da Investigação Digital</h2>
    <p>Mergulhe no universo da cibersegurança avançada e análise de sistemas com o Investigador Místico. Nossa equipe de elite está na vanguarda da tecnologia, explorando as fronteiras entre o real e o virtual para desvendar os mistérios do ciberespaço.</p>
  </section>

  <section>
    <h2>Arsenal Tecnológico</h2>
    <p>Nosso programa utiliza um conjunto sofisticado de ferramentas de última geração para capacitar nossos investigadores:</h2>
    <div class="tools-grid">
      <div class="tool-card">
        <h3>NebulaScan</h3>
        <p>Scanner de vulnerabilidades avançado com IA integrada para análise preditiva de ameaças.</p>
      </div>
      <div class="tool-card">
        <h3>QuantumCrypt</h3>
        <p>Sistema de criptografia quântica para comunicações ultra-seguras e invioláveis.</p>
      </div>
      <div class="tool-card">
        <h3>ShadowTracer</h3>
        <p>Ferramenta de rastreamento digital que mapeia a pegada online de alvos com precisão milimétrica.</p>
      </div>
      <div class="tool-card">
        <h3>MindMesh</h3>
        <p>Plataforma de análise comportamental que utiliza big data para prever padrões de atividade cibernética.</p>
      </div>
    </div>
  </section>

  <section>
    <h2>Elite Hacker Squad</h2>
    <p>Conheça os membros da nossa equipe de elite, liderada pelo lendário Investigador Místico:</p>
    <h2>equipe</h2>
    <div class="team-members">
      <div class="team-member">
        <img src="https://i.im.ge/2024/09/17/fJFQfa.IMG-20240917-WA0674.jpeg" alt="Investigador Místico" width="150" height="150">
        <h3>Investigador Místico</h3>
        <p>Líder e Visionário Sou perito em HTML, C++, CSS, PHP, Java, XML, MySQL, DDoS, Nmap, SQLmap, análise de metadados, engenharia e engenharia reversa</p>
      </div>
      <div class="team-member">
        <img src="https://i.im.ge/2024/09/17/fJufVf.IMG-20240914-WA0158.jpeg" alt="bima" width="150" height="150">
        <h3>Bima</h3>
        <p>Especialista em análise de Metadados, Engenharia Reversa e Engenharia social  Nmap sqlmap </p>
      </div>
      <div class="team-member">
        <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAgGBgcGBQgHBwcJCQgKDBQNDAsLDBkSEw8UHRofHh0aHBwgJC4nICIsIxwcKDcpLDAxNDQ0Hyc5PTgyPC4zNDL/2wBDAQkJCQwLDBgNDRgyIRwhMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjIyMjL/wAARCAQAAwADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwDxakooqhhRRRSGFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUlAC0UlFAC0UlFAC0UlFAC0UUlAC0UUUAFFFFABRRRQAUUUUAFFFJQAtFJRQAtJRRQAtFJRQAtFFJQAtFJRQAtJRRTAWikooAWikopALRSUUALRRRQAUUUUAFFFFABRSUUALRSUUALRSUUALRRRQAUUUUAFFJRQAtFJRQAtFFFABRRSUALRSUtABRRRQAUUUUAFFFJQAtFFFABRRRQAUUUUwFpKKKACiiikAUUUUAFFFFABRRRQAUUUUAFJS0lABRRRQAtJS0lAC0UUUAFJSmkoAKKKKYBRRRQAUUUUAFFFFIBaSlpKACiigUALRRSUALSUGigAooopgFFFFABRRRQAUUUtABSUtJSAKKWkoAKKKKYBRRRQAUUUUAFFFFIAopaSgAooopgFFFFIAooopgFFFFIAooopgFFLSUgCiiimAUUUUAFFFFABRRRQAtJQaKQBRS0lMBaKKKQBSUtFACUUUUwFpKWikAUUUUAFFFFMAooooAKKKKQBRSGigBaKKKACiiimAUUUUgCkpaSgAooooAWkpaSgBaSiigBaKKSgBaSiigBaSiigAooopgFFFFABRRRSAWkoooAWkoooAKKKKYBRRRQAUUUUAFFFFABS0lFAC0UUlIAooopgLSUUUAFFFFABRRRQAUUUUALSUtJSAKKKKYC0lLSUgCilpKAFopDRQAtFFJQAtJS0lAC0lFFMAooooAKKKKACiiigAooooAKKKKQC0UlAoAWiiigApKWkoAWkpaSgBaKKKACiiimAUUUUAFFFFIAooooAKKKKACiiigAooooAKSlooASig0UALSUUUALSUUUALSUtJQAUUtJQAUUtFACUUUUwCiiigAooooAKKKKACiiigAooooAKKKKACiiigAooooAKKKKAFooopAFFFJQAUUUUwCiiigAooooAKKKWkAUUUUAFFFJQAtFJRQAtFFFABRRRQAUUUlAC0lFFABRRRTAKKKKACiiigAooooAWkoopALSUUUAFFFFMBaKKSkAtFJRQAtJS0lAC0UUUAFFFFMAooooAKKKKQBRRRQAUUUUAFFFFABRRRQAUUUUAFJS0lAC0UUUAFFFFABRRRQAUUUUAFJS0UAJRRRTAKKKKACiiigAopaSkAtJS0YpgFFGKMUAJRS4ooASlxRiigAxRilopAJijFLRTATFGKWigBMUYpaKQCYoxS0UANIxRSmjFMBKKXFGKQBRRijFMApKU0lABS0lFIBaKSigBaSlpKAFopKKAFpKWkoAWiiigBKKDRTAKKKKAFooopAFJS0lAC0lFLQAUUUUAFFFFABRRRQAUlLSUALSUtFABRRRQAUUUUwCiiigAooooAKKKKQBRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRRRQAUUUUAFFFFABRSUtACUUUUwCilFLQA2inUUANop1FIBO1FFFMBaSiigAooooAKKKdQAlFLRSASilooASilooASilooASilooAbRTqKAG0U6k70AFFFFMBKWkooAWiiigBDSU6igBtFOopANop1NoAWkoopgLRSUUgCiiimAtFFJSAWiiigAooooAKKSloAKKKKACiiigAooooAKKKKACiiigAooooAKKKKYBRQaKACiiikAUUUUwCiiikAUUUUwCiiikAUUUUAFFFJQAtFFFABSUtFABRRRQAUUUUALRRRTAKKKKACiiigAopKUdKACiloxQA2lpaTFAC0UUUrgFFFFABRRRQAUUUUgCiiigAooooAKKKKACiiigAooooAMUUUUAFBoopgJ2pKdSUAJS0tFACUUtFACUUvakpgFFFFABRRRQAh6UlOooAbRTqKQCUUUUAFFFFABRRRQAUUlAoAWiiigAooooAKKKKACiiigAooooAKKKKACiiimAtJS0UAJRRRQAUUUUAFFFFABRRRQAUUUUgCiiigAooopgFFFFABRiilpAJilopKYC0UlFAC0UUYpAHNFLRTATFGKWikwExSiiii4C0UlFIBaSilxQAlFLRQAlFLRQAUUUUAFFFFABRiiigAooooAKKKKACiiigAooooAKSlooASilooASilpKACjNLikoAWikooAWkoopgFFFFFwExRS0nemAUUUUAFFFJQAtFFFABSUtGKAEopcUYoASiiikAUUUUAFFFFABRRRQAUUUUwCiiikAUUUUwCiiigBaKKKQCUUUUwCiiigAooooAKKKKACiiigAoopaAEpaKKACiiigAoopaAEopaBSASlpaKAEpaKSkAtJRS0AJS0UYoAKKMUYoAKKWigBKKWigAooooAKKKAKACijFGKACijFGKACijFGKACijFGKACijFGKACijFGKACijFGKACiiigAooooAD0ptOooASilooASilooASjFGKMUAFJS0UAJRRijFAC0UlFAAaTFOop3AbRSnrRTASilpKACiiigBD0opaKAEopaTFABRRiikAUUUUAFFFFMAooooAKKKKACiiigBaKKSkAUUUUwCiiigAooooAKKKWgBO9LRRQAUUUUAFFFLQAlLRS0gEopaKACiijFIBKXFFFABiiijFABRS0UAAooooAKKKMUAFFLiimAlFLRSASlpcUYoAbilpaKAEop1JQAlFOoxQA2inUUANop1FADaKdRQA2inUlACUUtFACUUtFACUU6koAQ0lONJQAlFLRQAlFLijFACUUtJQAUlLRQAlFLRQAlFLijFADTRTqKAEpKU0lAC02lop3ATtRS0UXASilpKYBRRRQAUmKWigBKKMUUAFFFFABRRRQAUUUUAFFFFAC0GiigBKKKKACiiigAxRS0UAFFFFABRRS4oAMUUtGKQBRRRSAKSlooAKKKMUAFFGKWgAxRRRQAUUUoFACUUuKMUAFFKOtGKACgdKWimAmKMUtFACYopaKACkpaKACiijFABRS4pMUDsFGKWlxQFhuKMU7FGKAsNxRinYoxQFhuKMU7FGKAsNxRinYpKAsJRQaMUBYSiloxQKwlFLijFIBKKXFJigAooooAMUYpaKAExSU6kxQAlGKdikoASkpaMUAFFFFACYoxS0UANopTSYoATFGKdikoASilpKAFoNFFMBuKKdikoASilpKYBRRRQAmKMUtFACYopaTvQAUUUUAFFFFAC0UUlABRRRigApaTFLQAUUUuKQCUUuKBQAUtFFFwCijFGKQBRS0YoASlxRiigAooooAKKUUUAJS4op1ADcUo6UtFMAxSYpaKACilooCwlFLRQOwYoxTsUYoCw3FGKWikOwYFGKWigQmKWjrRikAUUYoxRdjEopcUYouxBSUuKMUXYCUUuKMUXYBRRijFF2AlFLijFF2AlFLikxRdgFFLikouMKKKKLiDFGKWii4DMUuKXFGKYWExRinYpMUwsNopcc0UCsJRS4pKACkNLRQAmKKWigBtJTqQ0gEopcUlABRilpKADFJS0YoAKSlooASijFFABSUtFMBtFLRQAlFHeimAUneloxQAlFLikoAKKKKAFooxRikAYopTSUwCiilFABQKWikAUUUCkAUUtGKACkp1JQAdqKKKACilxRigAxRijFLigAFFLiigAoopcUwEopcUDrQFgxRinYoxSHYQDmlopKGAtFFFK4BRRijBouMKXFKBRQAmKMUuKMUrgIBS4FKBS0rgNop2KMUXCw3FGKdijFFwsNxRj2p2KMUXCw3HtRj2p1GKLhYbj2ox7U/8ACjFFx2GY9qTFSYpKLisxuKTFPoouFhmKMU/FJii4WG4pMU8jikxTuAmKTFOxSU7gJRTqbigAopcUmKACiiii4BTcU6immIZilxxTqQimFhtFLijFArCUhFLRQAmKCKWjFIBuKSn4pp60AJRS4ooADSYpaKAEoxS0lACUUtJigAopaSgBMUlOpDTASilx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" alt="Agente Quantum" width="150" height="150">
        <h3>Kazin</h3>
        <p>Kazin: Especialista em interpretação de diversas langs de programação da atualidade e praticante, entende conceitos básicos e avançados de pentester.</p>
      </div>

      </div>
      <div class="team-member">
        <img src="https://i.im.ge/2024/09/17/fJunIT.IMG-20240917-WA0576.jpeg" alt="AZRAEL" width="150" height="150">
        <h3>𝐀𝐙𝐑𝐀𝐄𝐋</</h3>
        <p>Especialista em se infiltrar e comsultar qualquer infomação necessráia tendo um conhecimento básico em todas as áreeas hacking,principalmente no móbile.</p>
      </div>

      <div class="team-member">
        <img src="https://via.placeholder.com/150" alt="Agente Matrix" width="150" height="150">
        <h3>Strategist</h3>
        <p>Tática e Planejamento de Operações</p>
      </div>
    </div>
  </section>
</div>

<section class="cta">
  <a href="#" id="open-modal">Inicie sua Jornada</a>
</section>

<div id="inscricao-modal">
  <div class="modal-content">
    <span class="close">&times;</span>
    <h2>Questionário de Iniciação</h2>
    <form id="inscricao-form">
      <input type="text" name="nome" placeholder="Nome do Iniciado" required>
      <input type="email" name="email" placeholder="E-mail de Contato" required>
      <textarea name="experiencia" placeholder="Descreva sua experiência com tecnologia e hacking" required></textarea>
      <textarea name="motivacao" placeholder="Por que deseja se juntar ao Investigador Místico?" required></textarea>
      <input type="tel" name="whatsapp" placeholder="WhatsApp para contato (+55 11 99689-6760)" required>
      <button type="submit">Enviar Candidatura</button>
    </form>
  </div>
</div>

<footer>
  <p>&copy; 2024 Investigador Místico. Todos os direitos reservados no multiverso digital.</p>
</footer>

<script>
document.addEventListener('DOMContentLoaded', (event) => {
    const modal = document.getElementById("inscricao-modal");
    const btn = document.getElementById("open-modal");
    const span = document.getElementsByClassName("close")[0];
    const form = document.getElementById("inscricao-form");

    btn.onclick = function() {
        modal.style.display = "block";
    }

    span.onclick = function() {
        modal.style.display = "none";
    }

    window.onclick = function(event) {
        if (event.target == modal) {
            modal.style.display = "none";
        }
    }

    form.onsubmit = function(e) {
        e.preventDefault();
        const formData = new FormData(form);
        const whatsapp = "+5511996896760";
        let message = "Nova inscrição para 🎩⚿_𝙀𝙇𝙄𝙏𝙀 𝙃𝘼𝘾𝙆𝙀𝙍_⚿🎩:\n\n";
        for (let [key, value] of formData.entries()) {
            message += `${key}: ${value}\n`;
        }

        const whatsappUrl = `https://wa.me/${whatsapp}?text=${encodeURIComponent(message)}`;
        window.open(whatsappUrl, '_blank');

        alert("Sua candidatura foi enviada com sucesso! Em breve entraremos em contato via WhatsApp.");
        modal.style.display = "none";
        form.reset();
    }
});
</script>

</body></html>
