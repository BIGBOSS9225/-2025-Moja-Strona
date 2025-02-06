# -2025-Moja-Strona
Strona "Moja Strona" to responsywna witryna oparta na HTML, CSS i JS. Zawiera trzy podstrony: główną, "O stronie głównej" z dodatkowymi informacjami oraz "Podstrona jawa" w języku jawa. Nawigacja z przyciskiem hamburgera ułatwia korzystanie na urządzeniach mobilnych.

index.html:

<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Strona Główna</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="container">
      <h1>Strona główna</h1>
      <button class="menu-toggle" aria-label="Przełącz nawigację">☰</button>
      <nav>
        <ul>
          <li><a href="about.html">O stronie głównej</a></li>
          <li><a href="jawa.html">Podstrona jawa</a></li>
        </ul>
      </nav>
    </div>
  </header>
  <main class="container">
    <p>To jest strona główna. Znajdziesz tutaj linki do różnych podstron.</p>
  </main>
  <footer>
    <div class="container">
      <p>&copy; 2025 Moja Strona</p>
    </div>
  </footer>
  <script src="script.js"></script>
</body>
</html>

about.html:

<!DOCTYPE html>
<html lang="pl">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>O nas</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="container">
      <h1>O stronie głównej</h1>
      <button class="menu-toggle" aria-label="Przełącz nawigację">☰</button>
      <nav>
        <ul>
          <li><a href="index.html">Strona Główna</a></li>
          <li><a href="jawa.html">Podstrona jawa</a></li>
        </ul>
      </nav>
    </div>
  </header>
  <main class="container">
    <p>na tej podstronie znajdziesz informacje na temat strony głównej.</p>
  </main>
  <footer>
    <div class="container">
      <p>&copy; 2025 Moja Strona</p>
    </div>
  </footer>
  <script src="script.js"></script>
</body>
</html>

jawa.html:

<!DOCTYPE html>
<html lang="jv">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Strona Jawa</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <div class="container">
      <h1>Podstrona jawa</h1>
      <button class="menu-toggle" aria-label="Przełącz nawigację">☰</button>
      <nav>
        <ul>
          <li><a href="index.html">Strona Główna</a></li>
          <li><a href="about.html">O stronie głównej</a></li>
        </ul>
      </nav>
    </div>
  </header>
  <main class="container">
    <p>
      Ta podstrona to podstrona strony głównej została napisana w języku jawa
    </p>
  </main>
  <footer>
    <div class="container">
      <p>&copy; 2025 Moja Strona</p>
    </div>
  </footer>
  <script src="script.js"></script>
</body>
</html>

style.css:

/* Reset i podstawowe ustawienia */
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    background: #f4f4f4;
    color: #333;
  }
  
  /* Kontener do centrowania zawartości */
  .container {
    width: 90%;
    max-width: 1200px;
    margin: auto;
  }
  
  /* Nagłówek */
  header {
    background-color: #333;
    color: #fff;
    padding: 10px 0;
  }
  
  header .container {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
  }
  
  header h1 {
    margin: 0;
    font-size: 1.5em;
  }
  
  /* Przycisk hamburger dla urządzeń mobilnych */
  .menu-toggle {
    display: none;
    background: none;
    border: none;
    color: #fff;
    font-size: 1.5em;
    cursor: pointer;
  }
  
  /* Nawigacja */
  nav ul {
    list-style: none;
    display: flex;
  }
  
  nav ul li {
    margin-left: 15px;
  }
  
  nav ul li:first-child {
    margin-left: 0;
  }
  
  nav ul li a {
    color: #fff;
    text-decoration: none;
    padding: 8px 12px;
    transition: background-color 0.3s ease;
  }
  
  nav ul li a:hover {
    background-color: #575757;
    border-radius: 4px;
  }
  
  /* Główna zawartość */
  main {
    background: #fff;
    padding: 20px;
    margin-top: 20px;
  }
  
  /* Stopka */
  footer {
    background-color: #333;
    color: #fff;
    text-align: center;
    padding: 10px 0;
    margin-top: 20px;
  }
  
  /* Style responsywne */
  @media (max-width: 768px) {
    header .container {
      flex-direction: column;
      align-items: flex-start;
    }
    
    .menu-toggle {
      display: block;
    }
    
    nav {
      width: 100%;
      display: none;
    }
    
    nav.active {
      display: block;
    }
    
    nav ul {
      flex-direction: column;
      width: 100%;
    }
    
    nav ul li {
      margin: 5px 0;
    }
    
    nav ul li a {
      display: block;
      width: 100%;
    }
  }

  script.js:

  // script.js

document.addEventListener('DOMContentLoaded', function() {
  const menuToggle = document.querySelector('.menu-toggle');
  const nav = document.querySelector('nav');
  
  if (menuToggle && nav) {
    menuToggle.addEventListener('click', function() {
      nav.classList.toggle('active');
    });
  }
});
