
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Consultorio Nutricional</title>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700&display=swap" rel="stylesheet">

<style>
:root{
  --verde:#1abc9c;
  --verde-oscuro:#148f77;
  --fondo:#eef3f6;
  --texto:#2c3e50;
  --sombra:0 15px 40px rgba(0,0,0,.12);
}

*{box-sizing:border-box;font-family:'Montserrat',sans-serif}

body{
  margin:0;
  background:var(--fondo);
  color:var(--texto);
}

/* HEADER */
header{
  background:linear-gradient(135deg,var(--verde),var(--verde-oscuro));
  color:white;
  padding:50px 20px;
  text-align:center;
}
header h1{margin:0;font-size:3rem}
header p{margin-top:10px;font-size:1.1rem;opacity:.9}

/* CONTENEDOR GENERAL */
.wrapper{
  width:95%;
  max-width:1600px;
  margin:auto;
  padding:40px 0;
}

/* GRID PRINCIPAL */
.main-grid{
  display:grid;
  grid-template-columns:1.2fr 1.5fr;
  gap:40px;
}

/* TARJETAS GRANDES */
.card{
  background:white;
  border-radius:22px;
  padding:35px;
  box-shadow:var(--sombra);
}

/* TITULOS */
h2{
  margin-top:0;
  color:var(--verde-oscuro);
  font-size:1.8rem;
}

/* FORMULARIOS */
.form{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:15px;
  margin-bottom:25px;
}

.form input{
  padding:14px;
  border-radius:12px;
  border:1px solid #ccc;
  font-size:1rem;
}

.form button{
  grid-column:1/-1;
  padding:14px;
  border:none;
  border-radius:14px;
  background:var(--verde);
  color:white;
  font-size:1.1rem;
  font-weight:600;
  cursor:pointer;
}

.form button:hover{background:var(--verde-oscuro)}

/* TABLAS */
table{
  width:100%;
  border-collapse:collapse;
  margin-top:15px;
  font-size:.95rem;
}

th{
  background:var(--verde);
  color:white;
  padding:14px;
}

td{
  padding:14px;
  border-bottom:1px solid #eee;
  text-align:center;
}

tr:hover{background:#f8fdfc}

/* BOTONES */
.btn{
  padding:8px 14px;
  border:none;
  border-radius:10px;
  color:white;
  cursor:pointer;
  font-weight:600;
}
.edit{background:#f39c12}
.delete{background:#e74c3c}
.save{background:#27ae60}

/* BADGES IMC */
.badge{
  padding:6px 14px;
  border-radius:20px;
  color:white;
  font-weight:600;
}
.bajo{background:#f1c40f}
.normal{background:#2ecc71}
.alto{background:#e74c3c}

/* GRID INFERIOR */
.bottom-grid{
  display:grid;
  grid-template-columns:1fr 1fr;
  gap:40px;
  margin-top:40px;
}

/* RUTINAS */
.rutina{
  background:#ecfdf5;
  border-left:8px solid var(--verde);
  padding:20px;
  border-radius:14px;
  margin-bottom:15px;
  line-height:1.6;
}

/* FOOTER */
footer{
  background:var(--verde-oscuro);
  color:white;
  text-align:center;
  padding:20px;
  margin-top:50px;
}
</style>
</head>

<body>

<header>
<h1>Consultorio Nutricional</h1>
<p>Evaluación corporal • Control de salud • Orientación personalizada</p>
</header>

<div class="wrapper">

<div class="main-grid">

<!-- PACIENTES -->
<div class="card">
<h2>Registro de Pacientes</h2>

<div class="form">
<input id="pnombre" placeholder="Nombre completo">
<input id="pedad" type="number" placeholder="Edad">
<input id="pmeta" placeholder="Objetivo del paciente">
<button onclick="guardarPaciente()">Guardar paciente</button>
</div>

<table>
<thead>
<tr><th>Nombre</th><th>Edad</th><th>Meta</th><th>Acciones</th></tr>
</thead>
<tbody id="pacientesTabla"></tbody>
</table>
</div>

<!-- IMC -->
<div class="card">
<h2>Evaluación IMC</h2>

<div class="form">
<input id="inombre" placeholder="Nombre del paciente">
<input id="ipeso" type="number" placeholder="Peso (kg)">
<input id="ialtura" type="number" placeholder="Altura (m)">
<button onclick="guardarIMC()">Calcular y guardar</button>
</div>

<table>
<thead>
<tr>
<th>Paciente</th><th>IMC</th><th>Estado</th><th>Recomendación</th><th>Acciones</th>
</tr>
</thead>
<tbody id="imcTabla"></tbody>
</table>
</div>

</div>

<div class="bottom-grid">

<!-- BENEFICIOS -->
<div class="card">
<h2>Beneficios de un Estilo de Vida Saludable</h2>
<table>
<tbody>
<tr><td>1</td><td>Mejora la salud cardiovascular</td></tr>
<tr><td>2</td><td>Aumenta la energía diaria</td></tr>
<tr><td>3</td><td>Fortalece el sistema inmunológico</td></tr>
<tr><td>4</td><td>Regula el peso corporal</td></tr>
<tr><td>5</td><td>Reduce el estrés y ansiedad</td></tr>
<tr><td>6</td><td>Mejora la calidad del sueño</td></tr>
<tr><td>7</td><td>Previene enfermedades crónicas</td></tr>
<tr><td>8</td><td>Fortalece músculos y huesos</td></tr>
<tr><td>9</td><td>Mejora la digestión</td></tr>
<tr><td>10</td><td>Aumenta la concentración</td></tr>
<tr><td>11</td><td>Mejora la postura</td></tr>
<tr><td>12</td><td>Incrementa la autoestima</td></tr>
<tr><td>13</td><td>Mejora la movilidad</td></tr>
<tr><td>14</td><td>Reduce riesgo de diabetes</td></tr>
<tr><td>15</td><td>Regula la presión arterial</td></tr>
<tr><td>16</td><td>Favorece la longevidad</td></tr>
<tr><td>17</td><td>Mejora la respiración</td></tr>
<tr><td>18</td><td>Fortalece la salud mental</td></tr>
<tr><td>19</td><td>Aumenta la productividad</td></tr>
<tr><td>20</td><td>Mejora la calidad de vida</td></tr>
</tbody>
</table>
</div>

<!-- RUTINAS -->
<div class="card">
<h2>Rutinas y Orientación Física</h2>

<div class="rutina">
<b>Bajar peso</b><br>
• Cardio 40–50 min (caminar, bicicleta, elíptica)<br>
• Alimentación balanceada<br>
• Hidratación constante<br>
• Rutina 5 días por semana
</div>

<div class="rutina">
<b>Subir masa muscular</b><br>
• Entrenamiento de fuerza 4–6 días<br>
• Aumento progresivo de cargas<br>
• Descanso adecuado<br>
• Consumo adecuado de proteínas
</div>

<div class="rutina">
<b>Tonificación</b><br>
• Fuerza + ejercicios funcionales<br>
• Series medias y altas repeticiones<br>
• Trabajo de core y estabilidad
</div>

<div class="rutina">
<b>Salud general</b><br>
• Caminatas diarias<br>
• Estiramientos<br>
• Movilidad articular<br>
• Actividad moderada constante
</div>

<div class="rutina">
<b>Resistencia física</b><br>
• Correr, nadar o ciclismo<br>
• Sesiones progresivas<br>
• Control de respiración
</div>

</div>

</div>

</div>

<footer>
Consultorio Nutricional © 2026
</footer>

<script>
let pacientes=[], imcs=[];
let editP=-1, editI=-1;

/* PACIENTES */
function guardarPaciente(){
  let obj={n:pnombre.value,e:pedad.value,m:pmeta.value};
  editP>=0?pacientes[editP]=obj:pacientes.push(obj);
  editP=-1;
  renderPacientes();
}

function renderPacientes(){
  pacientesTabla.innerHTML="";
  pacientes.forEach((p,i)=>{
    pacientesTabla.innerHTML+=`
    <tr>
    <td>${p.n}</td><td>${p.e}</td><td>${p.m}</td>
    <td>
      <button class="btn edit" onclick="editarPaciente(${i})">Editar</button>
      <button class="btn delete" onclick="pacientes.splice(${i},1);renderPacientes()">Eliminar</button>
    </td>
    </tr>`;
  });
}

function editarPaciente(i){
  let p=pacientes[i];
  pnombre.value=p.n; pedad.value=p.e; pmeta.value=p.m;
  editP=i;
}

/* IMC */
function guardarIMC(){
  let imc=(ipeso.value/(ialtura.value**2)).toFixed(2);
  let estado=imc<18.5?"Bajo peso":imc<25?"Normal":"Sobrepeso";
  let clase=estado=="Bajo peso"?"bajo":estado=="Normal"?"normal":"alto";
  let rec=estado=="Bajo peso"?"Aumentar calorías y fuerza":estado=="Normal"?"Mantener hábitos":"Reducir azúcares y cardio";
  let obj={n:inombre.value,imc,estado,clase,rec};
  editI>=0?imcs[editI]=obj:imcs.push(obj);
  editI=-1;
  renderIMC();
}

function renderIMC(){
  imcTabla.innerHTML="";
  imcs.forEach((x,i)=>{
    imcTabla.innerHTML+=`
    <tr>
    <td>${x.n}</td>
    <td>${x.imc}</td>
    <td><span class="badge ${x.clase}">${x.estado}</span></td>
    <td>${x.rec}</td>
    <td>
      <button class="btn edit" onclick="editarIMC(${i})">Editar</button>
      <button class="btn delete" onclick="imcs.splice(${i},1);renderIMC()">Eliminar</button>
    </td>
    </tr>`;
  });
}

function editarIMC(i){
  let x=imcs[i];
  inombre.value=x.n;
  ipeso.value="";
  ialtura.value="";
  editI=i;
}
</script>

</body>
</html>
