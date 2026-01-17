# nutricion-
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Consultorio Nutricional</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

<style>
*{
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}
body{
    margin:0;
    background:#f2f6f9;
    color:#2c3e50;
}
header{
    background:linear-gradient(135deg,#2ecc71,#27ae60);
    color:white;
    padding:40px;
    text-align:center;
}
header h1{
    margin:0;
    font-size:2.5em;
}
header p{
    margin-top:10px;
    font-size:1.1em;
}
.container{
    width:90%;
    max-width:1200px;
    margin:auto;
}
.card{
    background:white;
    padding:25px;
    margin:30px 0;
    border-radius:12px;
    box-shadow:0 10px 25px rgba(0,0,0,0.08);
}
h2{
    margin-top:0;
    color:#27ae60;
}
input{
    padding:10px;
    margin:5px;
    border-radius:8px;
    border:1px solid #ccc;
    width:200px;
}
button{
    padding:10px 15px;
    border:none;
    border-radius:8px;
    background:#27ae60;
    color:white;
    font-weight:600;
    cursor:pointer;
}
button:hover{
    background:#1e8449;
}
table{
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}
th{
    background:#27ae60;
    color:white;
    padding:10px;
}
td{
    padding:10px;
    text-align:center;
    border-bottom:1px solid #ddd;
}
.section-title{
    margin-top:30px;
    font-weight:600;
}
footer{
    background:#1e8449;
    color:white;
    text-align:center;
    padding:15px;
    margin-top:40px;
}
.tag{
    padding:5px 10px;
    border-radius:20px;
    color:white;
    font-size:0.85em;
}
.bajo{background:#f1c40f;}
.normal{background:#2ecc71;}
.alto{background:#e74c3c;}
</style>
</head>

<body>

<header>
<h1>Consultorio Nutricional</h1>
<p>Cuidamos tu salud, mejoramos tu calidad de vida</p>
</header>

<div class="container">

<div class="card">
<h2>Registro de Pacientes</h2>

<input type="text" id="nombre" placeholder="Nombre">
<input type="number" id="edad" placeholder="Edad">
<input type="text" id="meta" placeholder="Meta">
<button onclick="agregarPaciente()">Agregar</button>

<table>
<thead>
<tr>
<th>Nombre</th><th>Edad</th><th>Meta</th><th>Acciones</th>
</tr>
</thead>
<tbody id="tablaPacientes"></tbody>
</table>

<h3 class="section-title">Historial</h3>
<table>
<tr><th>Nombre</th><th>Edad</th><th>Meta</th></tr>
<tbody id="historialPacientes"></tbody>
</table>
</div>

<div class="card">
<h2>Cálculo de IMC</h2>

<input type="text" id="nombreIMC" placeholder="Nombre">
<input type="number" id="peso" placeholder="Peso (kg)">
<input type="number" id="altura" placeholder="Altura (m)">
<button onclick="calcularIMC()">Calcular</button>

<table>
<thead>
<tr>
<th>Nombre</th>
<th>IMC</th>
<th>Estado</th>
<th>Recomendaciones</th>
<th>Acciones</th>
</tr>
</thead>
<tbody id="tablaIMC"></tbody>
</table>

<h3 class="section-title">Historial IMC</h3>
<table>
<tr><th>Nombre</th><th>IMC</th><th>Estado</th></tr>
<tbody id="historialIMC"></tbody>
</table>
</div>

<div class="card">
<h2>Beneficios de un Estilo de Vida Saludable</h2>
<table>
<tr><th>#</th><th>Beneficio</th></tr>
<tbody>
<script>
const beneficios=[
"Mejora la salud cardiovascular","Aumenta la energía","Refuerza el sistema inmune",
"Controla el peso","Reduce el estrés","Mejora el sueño","Previene enfermedades",
"Fortalece músculos","Mejora la digestión","Aumenta la concentración",
"Reduce ansiedad","Mejora la autoestima","Mayor longevidad","Mejor movilidad",
"Regula la presión","Mejora la respiración","Reduce riesgo de diabetes",
"Salud mental","Bienestar general","Mayor calidad de vida"
];
beneficios.forEach((b,i)=>{
document.write(`<tr><td>${i+1}</td><td>${b}</td></tr>`);
});
</script>
</tbody>
</table>
</div>

<div class="card">
<h2>Rutinas de Ejercicio según la Meta</h2>
<table>
<tr><th>Meta</th><th>Rutina Recomendada</th></tr>
<tr><td>Bajar peso</td><td>Cardio 30–40 min + dieta balanceada</td></tr>
<tr><td>Subir masa muscular</td><td>Entrenamiento de fuerza 4–5 días</td></tr>
<tr><td>Tonificar</td><td>Ejercicios funcionales y resistencia</td></tr>
<tr><td>Resistencia</td><td>Correr, nadar o bicicleta</td></tr>
<tr><td>Salud general</td><td>Yoga, caminatas y estiramientos</td></tr>
</table>
</div>

</div>

<footer>
<p>Consultorio Nutricional © 2026</p>
</footer>

<script>
let pacientes=[], imcs=[];

function agregarPaciente(){
    const n=nombre.value,e=edad.value,m=meta.value;
    pacientes.push({n,e,m});
    renderPacientes();
}

function renderPacientes(){
    tablaPacientes.innerHTML="";
    historialPacientes.innerHTML="";
    pacientes.forEach((p,i)=>{
        tablaPacientes.innerHTML+=`
        <tr><td>${p.n}</td><td>${p.e}</td><td>${p.m}</td>
        <td><button onclick="pacientes.splice(${i},1);renderPacientes()">Eliminar</button></td></tr>`;
        historialPacientes.innerHTML+=`<tr><td>${p.n}</td><td>${p.e}</td><td>${p.m}</td></tr>`;
    });
}

function calcularIMC(){
    let imc=(peso.value/(altura.value**2)).toFixed(2);
    let estado="", clase="", rec="";
    if(imc<18.5){estado="Bajo peso";clase="bajo";rec="Más proteínas, 5 comidas, fuerza";}
    else if(imc<25){estado="Normal";clase="normal";rec="Mantener hábitos saludables";}
    else{estado="Sobrepeso";clase="alto";rec="Menos azúcares, cardio, agua";}
    imcs.push({n:nombreIMC.value,imc,estado,clase,rec});
    renderIMC();
}

function renderIMC(){
    tablaIMC.innerHTML="";
    historialIMC.innerHTML="";
    imcs.forEach((i,x)=>{
        tablaIMC.innerHTML+=`
        <tr><td>${i.n}</td><td>${i.imc}</td>
        <td><span class="tag ${i.clase}">${i.estado}</span></td>
        <td>${i.rec}</td>
        <td><button onclick="imcs.splice(${x},1);renderIMC()">Eliminar</button></td></tr>`;
        historialIMC.innerHTML+=`<tr><td>${i.n}</td><td>${i.imc}</td><td>${i.estado}</td></tr>`;
    });
}
</script>

</body>
</html>
