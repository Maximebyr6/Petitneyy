<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <title>Pour Chelsea, le petit Neyy</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #fcb1ab, #f6d365);
      font-family: 'Segoe UI', sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      overflow: hidden;
      text-align: center;
      color: #fff;
    }

    h1 {
      font-size: 2.3em;
      margin-bottom: 40px;
      animation: fadeIn 1s ease;
    }

    .buttons {
      display: flex;
      gap: 20px;
      animation: fadeIn 1s ease;
    }

    button {
      padding: 15px 35px;
      font-size: 1.1em;
      border: none;
      border-radius: 20px;
      cursor: pointer;
      transition: 0.3s ease;
      box-shadow: 0 5px 15px rgba(0,0,0,0.2);
    }

    .yes {
      background-color: #88e0a2;
      color: #fff;
    }

    .no {
      background-color: #f06292;
      color: #fff;
    }

    #reaction {
      margin-top: 30px;
      font-size: 1.6em;
      display: none;
      animation: fadeIn 1s ease;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .heart {
      position: absolute;
      font-size: 30px;
      animation: float 2s ease-out forwards;
      pointer-events: none;
    }

    @keyframes float {
      0% {
        transform: translateY(0) scale(1);
        opacity: 1;
      }
      100% {
        transform: translateY(-200px) scale(1.5);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <h1 id="question">Tu m’aimes Chelsea ?</h1>
  <div class="buttons">
    <button class="yes" onclick="answer(true)">Oui</button>
    <button class="no" onclick="answer(false)">Non</button>
  </div>
  <div id="reaction"></div>

  <script>
    const questions = [
      "Tu m’aimes Chelsea ?",
      "Tu préfères un massage ou un câlin ce soir ?",
      "Est-ce que tu veux un bisou là tout de suite ?",
      "Est-ce que tu me trouves sexy tous les jours ?",
      "Tu penses à moi même quand t’es énervée ?",
      "Tu veux qu’on fasse des bêtises ce soir ?",
      "Tu préfères dormir ou être dans mes bras ?",
      "T’as déjà stalké mon ex ?",
      "Tu m’autorises à regarder d’autres filles ?",
      "Tu veux que je t’appelle 'le petit Neyy' ce soir ?",
      "Tu trouves que je suis plus beau que ton ex ?",
      "Tu préfères moi ou une pizza à volonté ?",
      "Tu penses encore à Elena ? (attention à ta réponse...)",
      "Tu veux me faire un strip-tease ce week-end ?",
      "Tu serais jalouse si une fille me draguait ?",
      "Est-ce que je te rends heureuse ?",
      "Tu veux partir en week-end rien que nous deux ?",
      "Tu m’aimes même quand je suis relou ?",
      "Tu préfères un câlin ou une claque aux fesses ?",
      "T’es prête à m’aimer toute ta vie ?"
    ];

    const yesReplies = [
      "Je le savais, t'es à moi !",
      "J’apporte l’huile de massage alors !",
      "Tiens, viens le chercher !",
      "Toi t’as bon goût !",
      "Même fâchée t’es mignonne !",
      "Je vais pas te laisser dormir alors...",
      "Ok, viens dans mes bras maintenant.",
      "Je savais que t'étais curieuse !",
      "Ah ouais ? Mauvaise réponse Chelsea !",
      "Le petit Neyy devient coquin(e) là...",
      "Et de loin en plus !",
      "Bon choix, moi aussi je te mange !",
      "Tu rigoles j’espère hein ???",
      "C’est noté ! Prépare-toi !",
      "T’as intérêt à dire oui...",
      "Et moi je veux te garder pour toujours.",
      "Prépare ta valise bébé !",
      "Même relou je t’aime aussi !",
      "Je prends ça comme une invitation.",
      "C’est tout ce que je voulais entendre."
    ];

    const noReplies = [
      "Chelsea ?! Répète voir ?",
      "Tu veux pas de câlin ??",
      "Pas de bisou ? Je suis triste...",
      "Donc tu me trouves moche ?",
      "Tu me bloques dans ta tête ?",
      "Bon bah je dors alors hein...",
      "Même pas mes bras ?",
      "Pourquoi tu stalke alors ?",
      "Tu veux vraiment qu'on se fâche ?",
      "Oh oh… attitude suspecte !",
      "Quoi ?? Ton ex était mieux ?",
      "Ok… mais je garde la pizza pour moi !",
      "Je vais le dire à Elena, t’inquiète.",
      "Tu veux jouer à ce jeu-là ?",
      "Tu serais pas un peu possessive ?",
      "Moi aussi je suis triste maintenant.",
      "Tant pis, j’y vais tout seul.",
      "Mais t’as signé un contrat d’amour.",
      "Tu rates quelque chose là !",
      "Allez, redis-le correctement !"
    ];

    let index = 0;

    function answer(isYes) {
      if (index < questions.length) {
        document.getElementById("reaction").style.display = "block";
        document.getElementById("reaction").innerText = isYes ? yesReplies[index] : noReplies[index];

        if (isYes) showHearts();

        setTimeout(() => {
          index++;
          if (index < questions.length) {
            document.getElementById("question").innerText = questions[index];
            document.getElementById("reaction").style.display = "none";
          } else {
            document.getElementById("question").innerText = "T’as fini le jeu, le petit Neyy !";
            document.querySelector(".buttons").style.display = "none";
            document.getElementById("reaction").innerText = "Je t’aime fort Chelsea.";
          }
        }, 2500);
      }
    }

    function showHearts() {
      for (let i = 0; i < 6; i++) {
        const heart = document.createElement("div");
        heart.classList.add("heart");
        heart.innerText = "❤️";
        heart.style.left = `${Math.random() * 100}%`;
        heart.style.top = "80%";
        document.body.appendChild(heart);

        setTimeout(() => {
          heart.remove();
        }, 2000);
      }
    }
  </script>
</body>
</html>
