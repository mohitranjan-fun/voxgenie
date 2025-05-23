<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Simple Text-to-Speech App</title>
<style>
  body { font-family: Arial, sans-serif; padding: 20px; background: #f0f0f0; }
  textarea { width: 100%; height: 150px; font-size: 16px; padding: 10px; }
  button { margin-top: 15px; padding: 12px 25px; font-size: 18px; cursor: pointer; background: #4CAF50; color: white; border: none; border-radius: 5px; }
  button:hover { background: #45a049; }
</style>
</head>
<body>

<h2>Simple Text-to-Speech App</h2>
<textarea id="text" placeholder="Type text here..."></textarea>
<br />
<button onclick="speakText()">Speak 🗣️</button>

<script>
  function speakText() {
    const text = document.getElementById('text').value.trim();
    if (!text) {
      alert('Please enter some text to speak.');
      return;
    }
    const utterance = new SpeechSynthesisUtterance(text);
    utterance.lang = 'en-US'; // Change language if needed
    speechSynthesis.speak(utterance);
  }
</script>

</body>
</html>
