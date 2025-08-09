<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Flashcards for Kids</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      padding: 50px;
      background: #f0f8ff;
      color: #333;
    }
    #card {
      font-size: 3em;
      margin: 50px auto;
      padding: 30px 50px;
      border: 4px solid #007acc;
      border-radius: 15px;
      max-width: 400px;
      background: #e1f0ff;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
      user-select: none;
    }
    button {
      font-size: 1.5em;
      padding: 15px 30px;
      margin: 10px;
      border-radius: 10px;
      border: none;
      cursor: pointer;
      background: #007acc;
      color: white;
      transition: background 0.3s ease;
    }
    button:hover {
      background: #005f99;
    }
  </style>
</head>
<body>

  <h1>Flashcards: 3-Word Sentences</h1>
  <div id="card">Press Next to start</div>

  <div>
    <button id="prevBtn">Previous</button>
    <button id="nextBtn">Next</button>
  </div>

  <script>
    const sentences = [
      "I see cat", "You like apples", "We play ball", "He runs fast", "She eats pie",
      "Birds fly high", "Dogs bark loud", "Sun is bright", "Fish swim deep", "Rain falls down",
      "I love you", "They jump rope", "We read books", "You draw well", "He drinks milk",
      "Cats chase mice", "Kids laugh loud", "Cars move fast", "Flowers smell sweet", "Waves hit shore",
      "Mom cooks food", "Dad reads news", "Birds build nests", "Frogs jump high", "Stars shine bright",
      "I see stars", "You have toys", "We sing songs", "He likes cake", "She paints walls",
      "Dogs run fast", "Sun sets slow", "Fish swim fast", "Rain makes mud", "Kids play games",
      "I ride bike", "You swim well", "We eat rice", "He opens door", "She cleans room",
      "Cats sleep lots", "Birds sing sweet", "Cars honk loud", "Mom bakes bread", "Dad drives car",
      "I read book", "You write words", "We watch movie", "He jumps high", "She smiles bright",
      "Dogs chase balls", "Sun warms earth", "Fish catch worms", "Rain cools air", "Kids build forts",
      "I find shells", "You catch fish", "We plant trees", "He fixes bike", "She dances well",
      "Cats like milk", "Birds eat seeds", "Cars stop fast", "Mom hugs me", "Dad helps us",
      "I play drums", "You draw cats", "We love music", "He runs home", "She jumps rope",
      "Dogs sleep near", "Sun glows warm", "Fish hide rocks", "Rain falls soft", "Kids laugh more",
      "I see moon", "You have fun", "We cook dinner", "He reads book", "She writes notes",
      "Cats chase tails", "Birds fly south", "Cars drive slow", "Mom sings lullaby", "Dad tells stories",
      "I eat fruit", "You drink juice", "We jump high", "He plays guitar", "She smiles wide",
      "Dogs bark loud", "Sun shines bright", "Fish swim fast", "Rain pours hard", "Kids run free"
    ];

    let currentIndex = -1;
    const card = document.getElementById('card');
    const nextBtn = document.getElementById('nextBtn');
    const prevBtn = document.getElementById('prevBtn');

    function showSentence(index) {
      card.textContent = sentences[index];
    }

    nextBtn.addEventListener('click', () => {
      currentIndex++;
      if (currentIndex >= sentences.length) {
        currentIndex = 0; // loop to start
      }
      showSentence(currentIndex);
    });

    prevBtn.addEventListener('click', () => {
      currentIndex--;
      if (currentIndex < 0) {
        currentIndex = sentences.length - 1; // loop to end
      }
      showSentence(currentIndex);
    });
  </script>

</body>
</html>