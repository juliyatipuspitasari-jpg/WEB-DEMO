<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Website Fisika Mahasiswa</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Website Fisika</h1>
    <nav>
      <a href="index.html">Beranda</a>
      <a href="rumus.html">Rumus</a>
      <a href="kalkulator.html">Kalkulator</a>
    </nav>
  </header>

  <main>
    <h2>Selamat Datang!</h2>
    <p>Website ini dibuat untuk membantu mahasiswa fisika mempelajari <b>rumus dasar</b> 
       dan mencoba <b>kalkulator sederhana</b> langsung dari browser.</p>
  </main>

  <footer>
    <p>&copy; 2025 - Website Fisika Mahasiswa</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Rumus Fisika Dasar</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Rumus Fisika Dasar</h1>
    <nav>
      <a href="index.html">Beranda</a>
      <a href="rumus.html">Rumus</a>
      <a href="kalkulator.html">Kalkulator</a>
    </nav>
  </header>

  <main>
    <h2>Daftar Rumus</h2>
    <ul>
      <li><b>Energi Kinetik</b>: E = ½ m v²</li>
      <li><b>Hukum Ohm</b>: V = I × R</li>
      <li><b>Gaya Gravitasi</b>: F = G (m₁ m₂) / r²</li>
      <li><b>Momentum</b>: p = m v</li>
    </ul>
  </main>

  <footer>
    <p>&copy; 2025 - Website Fisika Mahasiswa</p>
  </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Kalkulator Fisika</title>
  <link rel="stylesheet" href="style.css">
  <script>
    function hitungOhm() {
      let I = parseFloat(document.getElementById("I").value);
      let R = parseFloat(document.getElementById("R").value);
      document.getElementById("V").innerText =
        (!isNaN(I) && !isNaN(R)) ? "V = " + (I * R) + " Volt" : "Masukkan angka!";
    }

    function hitungEnergi() {
      let m = parseFloat(document.getElementById("m").value);
      let v = parseFloat(document.getElementById("v").value);
      document.getElementById("E").innerText =
        (!isNaN(m) && !isNaN(v)) ? "E = " + (0.5 * m * v * v) + " Joule" : "Masukkan angka!";
    }

    function hitungMomentum() {
      let m = parseFloat(document.getElementById("m2").value);
      let v = parseFloat(document.getElementById("v2").value);
      document.getElementById("p").innerText =
        (!isNaN(m) && !isNaN(v)) ? "p = " + (m * v) + " kg·m/s" : "Masukkan angka!";
    }

    function hitungGravitasi() {
      let G = 6.67e-11;
      let m1 = parseFloat(document.getElementById("m1").value);
      let m2 = parseFloat(document.getElementById("m2g").value);
      let r = parseFloat(document.getElementById("r").value);
      document.getElementById("F").innerText =
        (!isNaN(m1) && !isNaN(m2) && !isNaN(r)) ? "F = " + (G * m1 * m2 / (r * r)) + " N" : "Masukkan angka!";
    }
  </script>
</head>
<body>
  <header>
    <h1>Kalkulator Fisika</h1>
    <nav>
      <a href="index.html">Beranda</a>
      <a href="rumus.html">Rumus</a>
      <a href="kalkulator.html">Kalkulator</a>
    </nav>
  </header>

  <main>
    <h2>Hukum Ohm</h2>
    <input type="number" id="I" placeholder="Arus (A)">
    <input type="number" id="R" placeholder="Hambatan (Ω)">
    <button onclick="hitungOhm()">Hitung</button>
    <p id="V"></p>

    <h2>Energi Kinetik</h2>
    <input type="number" id="m" placeholder="Massa (kg)">
    <input type="number" id="v" placeholder="Kecepatan (m/s)">
    <button onclick="hitungEnergi()">Hitung</button>
    <p id="E"></p>

    <h2>Momentum</h2>
    <input type="number" id="m2" placeholder="Massa (kg)">
    <input type="number" id="v2" placeholder="Kecepatan (m/s)">
    <button onclick="hitungMomentum()">Hitung</button>
    <p id="p"></p>

    <h2>Gaya Gravitasi</h2>
    <input type="number" id="m1" placeholder="Massa 1 (kg)">
    <input type="number" id="m2g" placeholder="Massa 2 (kg)">
    <input type="number" id="r" placeholder="Jarak (m)">
    <button onclick="hitungGravitasi()">Hitung</button>
    <p id="F"></p>
  </main>

  <footer>
    <p>&copy; 2025 - Website Fisika Mahasiswa</p>
  </footer>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #f0f8ff;
  text-align: center;
}

header {
  background: darkblue;
  color: white;
  padding: 15px;
}

nav a {
  color: white;
  margin: 0 15px;
  text-decoration: none;
}

nav a:hover {
  text-decoration: underline;
}

main {
  padding: 20px;
}

input {
  margin: 5px;
  padding: 8px;
  width: 200px;
}

button {
  padding: 8px 12px;
  margin-top: 5px;
  cursor: pointer;
}

button:hover {
  background: darkblue;
  color: white;
}

footer {
  margin-top: 30px;
  background: #ddd;
  padding: 10px;
}
