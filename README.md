# trishnaproposal
<!DOCTYPE html>
<html lang="bn">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>তৃষ্ণার জন্য প্রপোজাল</title>
  <style>
    body {
      font-family: 'SolaimanLipi', sans-serif;
      background-color: #fff8f0;
      color: #4b2e2e;
      padding: 40px;
      max-width: 700px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      border-radius: 20px;
      text-align: justify;
    }
    h1 {
      text-align: center;
      color: #c0392b;
    }
    .signature {
      margin-top: 40px;
      text-align: right;
      font-style: italic;
    }
    .button {
      display: block;
      margin: 30px auto;
      background-color: #c0392b;
      color: white;
      padding: 12px 24px;
      text-decoration: none;
      border-radius: 8px;
      font-size: 18px;
      width: max-content;
      cursor: pointer;
      border: none;
    }
    .button:hover {
      background-color: #a93226;
    }
    img {
      display: block;
      margin: 20px auto;
      max-width: 100%;
      border-radius: 15px;
    }
    .quiz-container {
      margin-top: 30px;
      border: 1px solid #c0392b;
      padding: 20px;
      border-radius: 15px;
      background-color: #ffe6e1;
    }
    .question {
      font-weight: bold;
      margin-bottom: 10px;
    }
    .options label {
      display: block;
      margin-bottom: 10px;
      cursor: pointer;
    }
    .result {
      margin-top: 20px;
      font-size: 20px;
      color: #c0392b;
      text-align: center;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>প্রিয় তৃষ্ণা,</h1>
  
  <img src="radhika.png" alt="রাধিকা" />
  <img src="couple.png" alt="Couple" />

  <p><strong>আমি তোমায় ভালোবাসি।</strong></p>
  <p>
    এই কথাটা দিয়েই শুরু করতে চেয়েছিলাম। কারণ আমার মনের সব কথা, সব অনুভূতির একটাই নাম—তুমি।<br><br>
    তোমার চোখের দিকে তাকালেই আমার মনে হয়, আমি আমার পুরো ভবিষ্যৎ দেখে ফেলেছি।<br>
    তুমি আমার জীবনে শুধুই একটা মেয়ে না, তুমি আমার সবকিছু।<br><br>
    মাঝে মাঝে হয়তো আমাদের মাঝে কিছু ভুল বোঝাবুঝি হয়, কিছু ছোটখাটো ঝগড়া হয়। কিন্তু সেগুলো ভালোবাসারই অংশ।<br>
    আমি যদি কোনো ভুল করে থাকি, যদি তোমার মনে কষ্ট দিয়ে থাকি, তাহলে সত্যিই দুঃখিত। আমি তো তোমারই, তাই আমায় সব সময় ক্ষমা করে দিও।<br><br>
    তুমি যদি আমার পাশে থাকতে চাও, আমি তোমার জন্য সারাজীবন অপেক্ষা করব।<br><br>
    <strong>I love you — Will you marry me?</strong>
  </p>

  <div class="signature">
    তোমার রাধিকার বাবা
  </div>

  <div class="quiz-container">
    <form id="quizForm">
      <div class="question">
        ১. তোমাদের মেয়ের নাম কী?
      </div>
      <div class="options">
        <label><input type="radio" name="q1" value="somapti" /> সমাপ্তি</label>
        <label><input type="radio" name="q1" value="radhika" /> রাধিকা</label>
      </div>

      <div class="question">
        ২. তুমি কি কাউন্টির কাছে তোমার রাধিকা র বাবা হোক?
      </div>
      <div class="options">
        <label><input type="radio" name="q2" value="yes" /> হ্যাঁ</label>
        <label><input type="radio" name="q2" value="no" /> না</label>
      </div>

      <div class="question">
        ৩. তুমি কি সত্যিই আমাকে ভালোবাসো?
      </div>
      <div class="options">
        <label><input type="radio" name="q3" value="yes" /> হ্যাঁ</label>
        <label><input type="radio" name="q3" value="no" /> না</label>
      </div>

      <div class="question">
        ৪. তুমি কি সারাজীবন আমার পাশে থাকতে চাও?
      </div>
      <div class="options">
        <label><input type="radio" name="q4" value="yes" /> হ্যাঁ</label>
        <label><input type="radio" name="q4" value="no" /> না</label>
      </div>

      <button type="submit" class="button">জমা দিন</button>
    </form>

    <div id="result" class="result"></div>
  </div>

  <script>
    const quizForm = document.getElementById('quizForm');
    const resultDiv = document.getElementById('result');

    quizForm.addEventListener('submit', function(event) {
      event.preventDefault();

      const answers = {
        q1: 'radhika',
        q2: 'yes',
        q3: 'yes',
        q4: 'yes'
      };

      const formData = new FormData(quizForm);
      let correctCount = 0;
      for (const [key, value] of formData.entries()) {
        if (answers[key] === value) {
          correctCount++;
        }
      }

      if (correctCount === Object.keys(answers).length) {
        resultDiv.textContent = 'সব উত্তর সঠিক! তোমার জন্য আমার প্রপোজাল: আমি তোমাকে সারাজীবন ভালোবাসবো। 💖 Will you marry me?';
      } else {
        resultDiv.textContent = 'দুঃখিত, সব উত্তর সঠিক হয়নি। একটু ভালো করে চিন্তা করে আবার চেষ্টা করো।';
      }
    });
  </script>
</body>
</html>
