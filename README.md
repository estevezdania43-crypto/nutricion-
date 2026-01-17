<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Consultorio Nutricional</title>

<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
:root{
    --verde:#2ecc71;
    --verde-oscuro:#1e8449;
    --gris:#f4f6f8;
    --texto:#2c3e50;
    --sombra:0 12px 30px rgba(0,0,0,.1);
}

*{box-sizing:border-box;font-family:Poppins}

body{
    margin:0;
    background:var(--gris);
    color:var(--texto);
}

header{
    background:linear-gradient(135deg,#2ecc71,#27ae60);
    color:white;
    padding:40px;
    text-align:center;
}

header h1{margin:0;font-size:2.6rem}
header p{opacity:.9}

.container{
    width:95%;
    max-width:1400px;
    margin:auto;
    padding:30px 0;
}

/* GRID PRINCIPAL */
.grid-main{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
}

/* TARJETAS */
.card{
    background:white;
    border-radius:16px;
    padding:25px;
    box-shadow:var(--sombra);
    transition:.3s;
}
.card:hover{transform:translateY(-4px)}

h2{
    color:var(--verde-oscuro);
    margin-top:0;
}

/* FORMULARIOS */
.form-group{
    display:flex;
    flex-wrap:wrap;
    gap:10px;
    margin-bottom:15px;
}

input{
    padding:10px;
    border-radius:10px;
    border:1px solid #ccc;
    flex:1;
    min-width:150px;
}

button{
    padding:10px 16px;
    border:none;
    border-radius:10px;
    background:var(--verde);
    color:white;
    font-weight:600;
    cursor:pointer;
    transition:.3s;
}
button:hover{background:var(--verde-oscuro)}

.btn-danger{background:#e74c3c}
.btn-warning{background:#f39c12}

/* TABLAS */
table{
    width:100%;
    border-collapse:collapse;
    margin-top:15px;
}

th{
    background:var(--verde);
    color:white;
    padding:10px;
}

td{
    padding:10px;
    text-align:center;
    border-bottom:1px solid #eee;
}

tr:hover{background:#f9f9f9}

/* ETIQUETAS IMC */
.badge{
    padding:6px 12px;
    border-radius:20px;
    color:white;
    font-size:.85rem;
    font-weight:600;
}
.bajo{background:#f1c40f}
.normal{background:#2ecc71}
.alto{background:#e74c3c}

/* GRID SECUNDARIO */
.grid-bottom{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:30px;
    margin-top:30px;
}

/* RUTINAS */
.rutina{
    background:#ecfdf5;
    border-left:6px solid var(--verde);
    padding:15px;
    margin-bottom:10px;
    border-radius:10px;
}

footer{
    background:var(--verde-oscuro);
    color:white;
    text-align:center;
    padding:15px;
    margin-top:40px;
}
</style>
</head>

<body>

<header>
<h1>Consultorio Nutricional Inteligente</h1>
<p>Evaluación, diagnóstico y recomendaciones personalizadas</p>
</header>

<div class="container">

<!-- GRID PRINCIPAL -->
<div class="grid-main">

<!-- PACIENTES -->
<div class="card">
<h2>Pacientes</h2>

<div class="form-group">
<input id="pNombre" placeholder="Nombre">
<input id="pEdad" type="number" placeholder="Edad">
<input id="pMeta" placeholder="Meta">
<button onclick="addPaciente()">Guardar</button>
</div>

<table>
<tr><th>Nombre</th><th>Edad</th><th>Meta</th><th>Acciones</th></tr>
<tbody id="tablaPacientes"></tbody>
</table>
</div>

<!-- IMC -->
<div class="card">
<h2>Evaluación IMC (IA)</h2>

<div class="form-group">
<input id="iNombre" placeholder="Nombre">
<input id="iPeso" type="number" placeholder="Peso kg">
<input id="iAltura" type="number" placeholder="Altura m">
<button onclick="addIMC()">Analizar</button>
</div>

<table>
<tr>
<th>Paciente</th><th>IMC</th><th>Estado</th><th>IA Recomienda</th><th></th>
</tr>
<tbody id="tablaIMC"></tbody>
</table>
</div>

</div>

<!-- GRID INFERIOR -->
<div class="grid-bottom">

<!-- BENEFICIOS -->
<div class="card">
<h2>20 Beneficios de una Vida Saludable</h2>
<table>
<tr><th>#</th><th>Beneficio</th></tr>
<tbody id="beneficios"></tbody>
</table>
</div>

<!-- RUTINAS -->
<div class="card">
<h2>Rutinas Inteligentes por Meta</h2>

<div class="rutina">
<b>Bajar peso</b><br>
• Cardio 40 min<br>
• Déficit calórico moderado<br>
• Hidratación constante<br>
• Dormir 7–8 h
</div>

<div class="rutina">
<b>Subir masa muscular</b><br>
• Pesas 4–5 días<br>
• Proteína suficiente<br>
• Progresión de cargas<br>
• Descanso activo
</div>

<div class="rutina">
<b>Tonificar</b><br>
• Fuerza + HIIT<br>
• Dieta equilibrada<br>
• Rutinas funcionales
</div>

<div class="rutina">
<b>Salud general</b><br>
• Caminatas diarias<br>
• Yoga / movilidad<br>
• Alimentación consciente
</div>

</div>

</div>

</div>

<footer>
Consultorio Nutricional © 2026
</footer>

<script>
let pacientes=[], imcs=[];

/* PACIENTES CRUD */
function addPaciente(){
    pacientes.push({
        n:pNombre.value,
        e:pEdad.value,
        m:pMeta.value
    });
    renderPacientes();
}

function renderPacientes(){
    tablaPacientes.innerHTML="";
    pacientes.forEach((p,i)=>{
        tablaPacientes.innerHTML+=`
        <tr>
        <td>${p.n}</td>
        <td>${p.e}</td>
        <td>${p.m}</td>
        <td>
        <button class="btn-danger" onclick="pacientes.splice(${i},1);renderPacientes()">X</button>
        </td>
        </tr>`;
    });
}

/* IMC CON LÓGICA IA */
function addIMC(){
    let imc=(iPeso.value/(iAltura.value**2)).toFixed(2);
    let estado,clase,rec;

    if(imc<18.5){
        estado="Bajo peso";clase="bajo";
        rec="Aumentar calorías, fuerza, más comidas";
    }else if(imc<25){
        estado="Normal";clase="normal";
        rec="Mantener hábitos y constancia";
    }else{
        estado="Sobrepeso";clase="alto";
        rec="Reducir azúcares, cardio y disciplina";
    }

    imcs.push({n:iNombre.value,imc,estado,clase,rec});
    renderIMC();
}

function renderIMC(){
    tablaIMC.innerHTML="";
    imcs.forEach((x,i)=>{
        tablaIMC.innerHTML+=`
        <tr>
        <td>${x.n}</td>
        <td>${x.imc}</td>
        <td><span class="badge ${x.clase}">${x.estado}</span></td>
        <td>${x.rec}</td>
        <td><button class="btn-danger" onclick="imcs.splice(${i},1);renderIMC()">X</button></td>
        </tr>`;
    });
}

/* BENEFICIOS */
const lista=[
"Mejor corazón","Más energía","Sistema inmune fuerte","Peso controlado",
"Menos estrés","Sueño profundo","Mejor digestión","Autoestima alta",
"Previene enfermedades","Músculos fuertes","Mayor movilidad",
"Salud mental","Longevidad","Mejor respiración","Concentración",
"Menos ansiedad","Vida activa","Mejor postura","Bienestar","Calidad de vida"
];
beneficios.innerHTML=lista.map((b,i)=>`<tr><td>${i+1}</td><td>${b}</td></tr>`).join("");
</script>

</body>
</html>
