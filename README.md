# peso-dos-planetas
Qual é o seu peso em outro planeta?
<!DOCTYPE html>
<html>
<head>
    <title>Seu peso em outros planetas</title>
</head>
<body>
    <h1>Descubra seu peso em outros planetas</h1>
    <label for="peso">Seu peso na Terra (kg):</label>
    <input type="number" id="peso" />
    <br><br>
    <label for="planeta">Escolha um planeta:</label>
    <select id="planeta">
        <option value="3.7">Mercúrio</option>
        <option value="8.87">Vênus</option>
        <option value="3.71">Marte</option>
        <option value="24.79">Júpiter</option>
        <option value="10.44">Saturno</option>
        <option value="8.69">Urano</option>
        <option value="11.15">Netuno</option>
    </select>
    <br><br>
    <button onclick="calcularPeso()">Calcular</button>

    <h2 id="resultado"></h2>

    <script>
        function calcularPeso() {
            const peso = parseFloat(document.getElementById("peso").value);
            const gravidadePlaneta = parseFloat(document.getElementById("planeta").value);
            const gravidadeTerra = 9.8;
            const pesoNovo = (peso * gravidadePlaneta / gravidadeTerra).toFixed(2);
            document.getElementById("resultado").textContent = "Seu peso seria: " + pesoNovo + " kg";
        }
    </script>
</body>
</html>
