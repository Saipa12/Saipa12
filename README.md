<!-- README.md -->

<div align="center">
  <h1>Привет! Я Сайпа 👋</h1>
  <p>Мне <span id="age"></span> год/лет</p>
  <p>Я C# Backend Developer</p>

  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
      color: #333;
    }
    .container {
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    h1 {
      color: #007acc;
    }
  </style>

  <script>
    function calculateAge(birthdate) {
      const birthDate = new Date(birthdate);
      const today = new Date();
      let age = today.getFullYear() - birthDate.getFullYear();
      const m = today.getMonth() - birthDate.getMonth();
      if (m < 0 || (m === 0 && today.getDate() < birthDate.getDate())) {
        age--;
      }
      return age;
    }

    document.addEventListener('DOMContentLoaded', () => {
      const age = calculateAge('2003-12-25');
      document.getElementById('age').innerText = age;
    });
  </script>
</div>
