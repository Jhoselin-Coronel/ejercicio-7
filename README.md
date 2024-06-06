
<html>
<head>
  <title>Demostración de la serie numérica</title>
</head>
<body>
  <h1>Demostración de la serie numérica $\sum_{n=1}^{\infty }\frac{1}{n^{2}}$ converge a $\frac{\pi^2}{16}$</h1>

  <h2>Resultados:</h2>
  <p>Para <strong>n=100</strong>, la suma es: <span id="result-100"></span></p>
  <p>Para <strong>n=1000</strong>, la suma es: <span id="result-1000"></span></p>
  <p>Para <strong>n=10000</strong>, la suma es: <span id="result-10000"></span></p>

  <p>El valor de $\frac{\pi^2}{16}$ es: <span id="pi-squared-16"></span></p>

  <script>
    // Para n=100
    let v100 = Array.from({ length: 100 }, (_, i) => i + 1);
    let term100 = v100.map(n => 1 / (n ** 2));
    let result100 = term100.reduce((acc, cur) => acc + cur, 0);
    document.getElementById('result-100').textContent = result100.toFixed(4);

    // Para n=1000
    let v1000 = Array.from({ length: 1000 }, (_, i) => i + 1);
    let term1000 = v1000.map(n => 1 / (n ** 2));
    let result1000 = term1000.reduce((acc, cur) => acc + cur, 0);
    document.getElementById('result-1000').textContent = result1000.toFixed(4);

    // Para n=10000
    let v10000 = Array.from({ length: 10000 }, (_, i) => i + 1);
    let term10000 = v10000.map(n => 1 / (n ** 2));
    let result10000 = term10000.reduce((acc, cur) => acc + cur, 0);
    document.getElementById('result-10000').textContent = result10000.toFixed(4);

    // Valor de π^2/16
    document.getElementById('pi-squared-16').textContent = (Math.PI ** 2 / 16).toFixed(4);
  </script>
</body>
</html>
