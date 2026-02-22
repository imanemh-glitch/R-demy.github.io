# Rédemy.github.io
<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<title>Rédemy - Plateforme E-Learning Réseau</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background: #f7f5fb;
    color: #333;
  }

  header {
    background: linear-gradient(90deg, #4a90e2, #ff6ec7);
    color: white;
    padding: 30px;
    text-align: center;
    font-size: 2em;
    font-weight: bold;
  }

  nav {
    background: #4a90e2;
    display: flex;
    justify-content: center;
    padding: 12px;
  }

  nav a {
    color: white;
    margin: 0 20px;
    text-decoration: none;
    font-weight: bold;
  }

  nav a:hover {
    color: #ff6ec7;
  }

  main {
    padding: 20px;
  }

  section {
    background: white;
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 15px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  }

  h2 {
    color: #4a90e2;
    text-align: center;
  }

  p {
    text-align: center;
    font-size: 1.1em;
  }

  .animation-box {
    width: 120px;
    height: 120px;
    background: #ff6ec7;
    border-radius: 20px;
    margin: 20px auto;
    position: relative;
    animation: bounce 3s infinite alternate;
  }

  @keyframes bounce {
    0% { top: 0; background-color: #ff6ec7; }
    50% { top: 50px; background-color: #4a90e2; }
    100% { top: 0; background-color: #ff6ec7; }
  }

  form {
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  form input, form button {
    width: 80%;
    padding: 10px;
    margin: 10px 0;
    border-radius: 5px;
    border: 1px solid #ccc;
    font-size: 1em;
  }

  form button {
    background: linear-gradient(90deg, #4a90e2, #ff6ec7);
    color: white;
    border: none;
    cursor: pointer;
    font-weight: bold;
  }

  form button:hover {
    opacity: 0.9;
  }

  .pdf-links a {
    display: block;
    margin: 10px auto;
    width: 80%;
    text-align: center;
    background: #4a90e2;
    color: white;
    text-decoration: none;
    padding: 12px;
    border-radius: 8px;
  }

  .pdf-links a:hover {
    background: #ff6ec7;
  }

</style>
</head>
<body>

<header>Rédemy - Plateforme E-Learning Réseau</header>

<nav>
  <a href="#accueil">Accueil</a>
  <a href="#objectif">Notre Objectif</a>
  <a href="#pourquoi">Pourquoi choisir Rédemy</a>
  <a href="#pdfs">PDFs</a>
</nav>

<main>
  <!-- Accueil -->
  <section id="accueil">
    <h2>Bienvenue sur Rédemy</h2>
    <p>Apprenez le réseau et l'informatique facilement grâce à notre plateforme E-Learning.</p>
    <div class="animation-box" title="Animation CSS3"></div>
  </section>

  <!-- Objectif -->
  <section id="objectif">
    <h2>Notre Objectif</h2>
    <p>Fournir des cours interactifs et accessibles pour comprendre les concepts réseau, les modèles OSI, et les commandes essentielles.</p>
  </section>

  <!-- Pourquoi choisir Rédemy -->
  <section id="pourquoi">
    <h2>Pourquoi choisir Rédemy</h2>
    <p>
      ✅ Contenu pédagogique structuré <br>
      ✅ Illustrations et schémas <br>
      ✅ Exercices pratiques et PDFs téléchargeables <br>
      ✅ Plateforme facile à utiliser et interactive
    </p>
  </section>

  <!-- PDFs Section avec formulaire -->
  <section id="pdfs">
    <h2>Téléchargez nos ressources PDF</h2>
    <p>Remplissez le formulaire avant de télécharger les PDF :</p>

    <form id="pdfForm">
      <input type="text" id="name" placeholder="Votre nom" required>
      <input type="email" id="email" placeholder="Votre email" required>
      <button type="submit">Accéder aux PDFs</button>
    </form>

    <div class="pdf-links" id="pdfLinks" style="display:none;">
      <a href="pdf/modele-osi.pdf" target="_blank">📄 PDF: Modèle OSI</a>
      <a href="pdf/commandes-reseau.pdf" target="_blank">📄 PDF: Bases des commandes réseau</a>
      <a href="pdf/reseau-complet.pdf" target="_blank">📄 PDF: Réseau complet</a>
    </div>
  </section>

</main>

<footer>
  &copy; 2026 Rédemy - Academy Réseau
</footer>

<script>
  // JavaScript avant la dépose des PDF
  const form = document.getElementById('pdfForm');
  const pdfLinks = document.getElementById('pdfLinks');

  form.addEventListener('submit', function(e){
    e.preventDefault();
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();

    if(name === "" || email === ""){
      alert("Veuillez remplir tous les champs avant de télécharger les PDFs !");
      return;
    }

    alert(`Merci ${name} !\nVous pouvez maintenant accéder aux PDF.`);
    pdfLinks.style.display = "block"; // Affiche les liens PDF après validation
    form.reset();
  });
</script>

</body>
</html>
