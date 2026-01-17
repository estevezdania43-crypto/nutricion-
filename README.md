
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Consultorio Nutricional Esteves</title>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --verde-primario: #1abc9c;
            --verde-oscuro: #148f77;
            --verde-claro: #d1f2eb;
            --fondo: #f8fbfc;
            --fondo-card: #ffffff;
            --texto: #2c3e50;
            --texto-claro: #7f8c8d;
            --borde: #e0e6e9;
            --sombra: 0 10px 30px rgba(0, 0, 0, 0.08);
            --sombra-hover: 0 15px 40px rgba(0, 0, 0, 0.12);
            --naranja: #f39c12;
            --rojo: #e74c3c;
            --azul: #3498db;
            --radius: 16px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Montserrat', sans-serif;
        }

        body {
            background-color: var(--fondo);
            color: var(--texto);
            line-height: 1.6;
            min-height: 100vh;
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, var(--verde-primario), var(--verde-oscuro));
            color: white;
            padding: 2.5rem 1.5rem;
            text-align: center;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url("data:image/svg+xml,%3Csvg width='100' height='100' viewBox='0 0 100 100' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath d='M11 18c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm48 25c3.866 0 7-3.134 7-7s-3.134-7-7-7-7 3.134-7 7 3.134 7 7 7zm-43-7c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm63 31c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM34 90c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zm56-76c1.657 0 3-1.343 3-3s-1.343-3-3-3-3 1.343-3 3 1.343 3 3 3zM12 86c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm28-65c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm23-11c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-6 60c2.21 0 4-1.79 4-4s-1.79-4-4-4-4 1.79-4 4 1.79 4 4 4zm29 22c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zM32 63c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm57-13c2.76 0 5-2.24 5-5s-2.24-5-5-5-5 2.24-5 5 2.24 5 5 5zm-9-21c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM60 91c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM35 41c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2zM12 60c1.105 0 2-.895 2-2s-.895-2-2-2-2 .895-2 2 .895 2 2 2z' fill='%23148f77' fill-opacity='0.1' fill-rule='evenodd'/%3E%3C/svg%3E");
            opacity: 0.2;
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .header h1 {
            font-size: 2.8rem;
            margin-bottom: 0.5rem;
            font-weight: 800;
            letter-spacing: -0.5px;
        }

        .header p {
            font-size: 1.2rem;
            opacity: 0.95;
            max-width: 700px;
            margin: 0 auto;
        }

        /* Contenedor principal */
        .container {
            width: 95%;
            max-width: 1600px;
            margin: 0 auto;
            padding: 2.5rem 0;
        }

        /* Grid principal */
        .main-grid {
            display: grid;
            grid-template-columns: 1fr 1.2fr;
            gap: 2.5rem;
            margin-bottom: 2.5rem;
        }

        /* Responsive */
        @media (max-width: 1100px) {
            .main-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Cards */
        .card {
            background-color: var(--fondo-card);
            border-radius: var(--radius);
            padding: 2rem;
            box-shadow: var(--sombra);
            transition: var(--transition);
            height: fit-content;
        }

        .card:hover {
            box-shadow: var(--sombra-hover);
        }

        .card-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .card h2 {
            color: var(--verde-oscuro);
            font-size: 1.6rem;
            font-weight: 700;
            margin: 0;
        }

        .card-icon {
            color: var(--verde-primario);
            font-size: 1.8rem;
        }

        /* Formularios */
        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .input-group {
            display: flex;
            flex-direction: column;
        }

        .input-group label {
            font-size: 0.9rem;
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--texto);
        }

        .form-input {
            padding: 0.9rem 1rem;
            border: 2px solid var(--borde);
            border-radius: 10px;
            font-size: 1rem;
            transition: var(--transition);
            background-color: #fcfdfd;
        }

        .form-input:focus {
            outline: none;
            border-color: var(--verde-primario);
            background-color: white;
        }

        .btn {
            padding: 0.9rem 1.5rem;
            border: none;
            border-radius: 10px;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 0.5rem;
            font-size: 1rem;
        }

        .btn-primary {
            background-color: var(--verde-primario);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--verde-oscuro);
        }

        .btn-block {
            width: 100%;
            grid-column: 1 / -1;
        }

        /* Tablas */
        .table-container {
            overflow-x: auto;
            margin-top: 1.5rem;
        }

        .table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.95rem;
        }

        .table th {
            background-color: var(--verde-primario);
            color: white;
            padding: 1rem;
            text-align: left;
            font-weight: 600;
        }

        .table td {
            padding: 1rem;
            border-bottom: 1px solid var(--borde);
        }

        .table tbody tr {
            transition: var(--transition);
        }

        .table tbody tr:hover {
            background-color: #f8fdfc;
        }

        /* Badges IMC */
        .badge {
            display: inline-block;
            padding: 0.4rem 0.9rem;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            text-align: center;
            min-width: 100px;
        }

        .badge-bajo {
            background-color: #fef9e7;
            color: #b7950b;
        }

        .badge-normal {
            background-color: #e8f8f1;
            color: #27ae60;
        }

        .badge-sobrepeso {
            background-color: #fdedec;
            color: #e74c3c;
        }

        /* Botones de acción */
        .btn-action {
            padding: 0.5rem 0.9rem;
            border-radius: 8px;
            border: none;
            font-weight: 600;
            cursor: pointer;
            transition: var(--transition);
            font-size: 0.85rem;
            display: inline-flex;
            align-items: center;
            gap: 0.4rem;
        }

        .btn-edit {
            background-color: #fef5e7;
            color: #f39c12;
        }

        .btn-edit:hover {
            background-color: #fdebd0;
        }

        .btn-delete {
            background-color: #fdedec;
            color: #e74c3c;
        }

        .btn-delete:hover {
            background-color: #fadbd8;
        }

        .btn-save {
            background-color: #e8f8f1;
            color: #27ae60;
        }

        .btn-save:hover {
            background-color: #d1f2eb;
        }

        .action-buttons {
            display: flex;
            gap: 0.5rem;
        }

        /* Grid inferior */
        .bottom-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2.5rem;
        }

        @media (max-width: 900px) {
            .bottom-grid {
                grid-template-columns: 1fr;
            }
        }

        /* Beneficios */
        .benefits-list {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1rem;
            margin-top: 1rem;
        }

        .benefit-item {
            background-color: #f9fcfb;
            padding: 1rem;
            border-radius: 10px;
            border-left: 4px solid var(--verde-primario);
            transition: var(--transition);
        }

        .benefit-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .benefit-number {
            display: inline-block;
            background-color: var(--verde-claro);
            color: var(--verde-oscuro);
            width: 28px;
            height: 28px;
            border-radius: 50%;
            text-align: center;
            line-height: 28px;
            font-weight: 700;
            margin-right: 0.5rem;
        }

        /* Rutinas */
        .routine {
            background-color: #f9fcfb;
            padding: 1.5rem;
            border-radius: 12px;
            border-left: 6px solid var(--verde-primario);
            margin-bottom: 1rem;
            transition: var(--transition);
        }

        .routine:hover {
            transform: translateX(5px);
        }

        .routine-title {
            color: var(--verde-oscuro);
            font-weight: 700;
            margin-bottom: 0.8rem;
            font-size: 1.1rem;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .routine-list {
            list-style-type: none;
        }

        .routine-list li {
            padding: 0.3rem 0;
            display: flex;
            align-items: flex-start;
        }

        .routine-list li::before {
            content: "•";
            color: var(--verde-primario);
            font-weight: bold;
            margin-right: 0.5rem;
        }

        /* Estadísticas */
        .stats-container {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .stat-card {
            background-color: white;
            border-radius: 12px;
            padding: 1.5rem;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }

        .stat-value {
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--verde-oscuro);
            margin-bottom: 0.5rem;
        }

        .stat-label {
            font-size: 0.9rem;
            color: var(--texto-claro);
            font-weight: 600;
        }

        /* Footer */
        .footer {
            background-color: var(--verde-oscuro);
            color: white;
            text-align: center;
            padding: 2rem;
            margin-top: 3rem;
        }

        .footer-content {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Mensajes */
        .message {
            padding: 1rem;
            border-radius: 10px;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            opacity: 0;
            transform: translateY(-10px);
            transition: all 0.5s ease;
        }

        .message.show {
            opacity: 1;
            transform: translateY(0);
        }

        .message-success {
            background-color: #e8f8f1;
            color: #27ae60;
            border-left: 4px solid #27ae60;
        }

        .message-error {
            background-color: #fdedec;
            color: #e74c3c;
            border-left: 4px solid #e74c3c;
        }

        .message-warning {
            background-color: #fef9e7;
            color: #f39c12;
            border-left: 4px solid #f39c12;
        }

        /* Responsive adicional */
        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.2rem;
            }
            
            .form-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-container {
                grid-template-columns: 1fr;
            }
            
            .card {
                padding: 1.5rem;
            }
        }

        /* Animaciones */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .card, .routine, .benefit-item {
            animation: fadeIn 0.5s ease-out forwards;
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="header-content">
            <h1><i class="fas fa-heartbeat"></i> Consultorio Nutricional ESTEVES</h1>
            <p>Evaluación integral • PROYECTO DE MODULO</p>
        </div>
    </header>

    <main class="container">
        <div id="messageContainer"></div>
        
        <div class="main-grid">
            <!-- Sección Pacientes -->
            <section class="card">
                <div class="card-header">
                    <h2><i class="fas fa-users card-icon"></i> Registro de Pacientes</h2>
                    <span class="badge badge-normal" id="pacientesCount">0 pacientes</span>
                </div>
                
                <div class="form-grid">
                    <div class="input-group">
                        <label for="pnombre">Nombre completo</label>
                        <input type="text" id="pnombre" class="form-input" placeholder="Ej: María González">
                    </div>
                    
                    <div class="input-group">
                        <label for="pedad">Edad</label>
                        <input type="number" id="pedad" class="form-input" placeholder="Ej: 32" min="1" max="120">
                    </div>
                    
                    <div class="input-group">
                        <label for="pmeta">Objetivo del paciente</label>
                        <input type="text" id="pmeta" class="form-input" placeholder="Ej: Bajar 10kg">
                    </div>
                    
                    <button id="guardarPacienteBtn" class="btn btn-primary btn-block">
                        <i class="fas fa-save"></i> Guardar paciente
                    </button>
                </div>
                
                <div class="table-container">
                    <table class="table">
                        <thead>
                            <tr>
                                <th>Nombre</th>
                                <th>Edad</th>
                                <th>Meta</th>
                                <th>Acciones</th>
                            </tr>
                        </thead>
                        <tbody id="pacientesTabla">
                            <!-- Datos se cargarán aquí -->
                        </tbody>
                    </table>
                </div>
            </section>

            <!-- Sección IMC -->
            <section class="card">
                <div class="card-header">
                    <h2><i class="fas fa-weight card-icon"></i> Evaluación IMC</h2>
                    <span class="badge badge-normal" id="imcCount">0 evaluaciones</span>
                </div>
                
                <div class="form-grid">
                    <div class="input-group">
                        <label for="inombre">Nombre del paciente</label>
                        <input type="text" id="inombre" class="form-input" placeholder="Buscar paciente...">
                        <div id="pacientesList" class="pacientes-autocomplete"></div>
                    </div>
                    
                    <div class="input-group">
                        <label for="ipeso">Peso (kg)</label>
                        <input type="number" id="ipeso" class="form-input" placeholder="Ej: 68.5" step="0.1" min="1" max="300">
                    </div>
                    
                    <div class="input-group">
                        <label for="ialtura">Altura (m)</label>
                        <input type="number" id="ialtura" class="form-input" placeholder="Ej: 1.65" step="0.01" min="0.5" max="2.5">
                    </div>
                    
                    <button id="calcularIMCBtn" class="btn btn-primary btn-block">
                        <i class="fas fa-calculator"></i> Calcular y guardar
                    </button>
                </div>
                
                <div class="stats-container">
                    <div class="stat-card">
                        <div class="stat-value" id="avgIMC">0.0</div>
                        <div class="stat-label">IMC Promedio</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="normalCount">0</div>
                        <div class="stat-label">Normales</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-value" id="alertaCount">0</div>
                        <div class="stat-label">Con alerta</div>
                    </div>
                </div>
                
                <div class="table-container">
                    <table class="table">
                        <thead>
                            <tr>
                                <th>Paciente</th>
                                <th>IMC</th>
                                <th>Estado</th>
                                <th>Recomendación</th>
                                <th>Acciones</th>
                            </tr>
                        </thead>
                        <tbody id="imcTabla">
                            <!-- Datos se cargarán aquí -->
                        </tbody>
                    </table>
                </div>
            </section>
        </div>

        <div class="bottom-grid">
            <!-- Beneficios -->
            <section class="card">
                <div class="card-header">
                    <h2><i class="fas fa-heart card-icon"></i> Beneficios de un Estilo de Vida Saludable</h2>
                </div>
                
                <div class="benefits-list">
                    <!-- Los beneficios se cargarán dinámicamente -->
                </div>
            </section>

            <!-- Rutinas -->
            <section class="card">
                <div class="card-header">
                    <h2><i class="fas fa-running card-icon"></i> Rutinas y Orientación Física</h2>
                </div>
                
                <div id="rutinasContainer">
                    <!-- Las rutinas se cargarán dinámicamente -->
                </div>
            </section>
        </div>
    </main>

    <footer class="footer">
        <div class="footer-content">
            <p><i class="fas fa-heartbeat"></i> Consultorio Nutricional © 2026</p>
            <p style="opacity: 0.8; margin-top: 0.5rem; font-size: 0.9rem;">Sistema de gestión integral para profesionales de la salud</p>
        </div>
    </footer>

    <script>
        // Variables globales
        let pacientes = JSON.parse(localStorage.getItem('nutri-pacientes')) || [];
        let imcs = JSON.parse(localStorage.getItem('nutri-imcs')) || [];
        let editPacienteIndex = -1;
        let editImcIndex = -1;
        
        // Lista de beneficios
        const beneficios = [
            "Mejora la salud cardiovascular",
            "Aumenta la energía diaria",
            "Fortalece el sistema inmunológico",
            "Regula el peso corporal",
            "Reduce el estrés y ansiedad",
            "Mejora la calidad del sueño",
            "Previene enfermedades crónicas",
            "Fortalece músculos y huesos",
            "Mejora la digestión",
            "Aumenta la concentración",
            "Mejora la postura",
            "Incrementa la autoestima",
            "Mejora la movilidad",
            "Reduce riesgo de diabetes",
            "Regula la presión arterial",
            "Favorece la longevidad",
            "Mejora la respiración",
            "Fortalece la salud mental",
            "Aumenta la productividad",
            "Mejora la calidad de vida"
        ];
        
        // Lista de rutinas
        const rutinas = [
            {
                titulo: "Bajar peso",
                icono: "fas fa-weight",
                items: [
                    "Cardio 40–50 min (caminar, bicicleta, elíptica)",
                    "Alimentación balanceada con déficit calórico",
                    "Hidratación constante (2-3 litros diarios)",
                    "Rutina 5 días por semana",
                    "Control de porciones y registro alimenticio"
                ]
            },
            {
                titulo: "Subir masa muscular",
                icono: "fas fa-dumbbell",
                items: [
                    "Entrenamiento de fuerza 4–6 días por semana",
                    "Aumento progresivo de cargas",
                    "Descanso adecuado (7-9 horas diarias)",
                    "Consumo adecuado de proteínas (1.6-2.2g/kg)",
                    "Superávit calórico controlado"
                ]
            },
            {
                titulo: "Tonificación",
                icono: "fas fa-user-check",
                items: [
                    "Fuerza + ejercicios funcionales",
                    "Series medias y altas repeticiones (12-15)",
                    "Trabajo de core y estabilidad",
                    "Ejercicios con peso corporal",
                    "Enfoque en forma y técnica"
                ]
            },
            {
                titulo: "Salud general",
                icono: "fas fa-heartbeat",
                items: [
                    "Caminatas diarias de 30 minutos",
                    "Estiramientos y movilidad articular",
                    "Actividad moderada constante",
                    "Alimentación balanceada y variada",
                    "Gestión del estrés y mindfulness"
                ]
            },
            {
                titulo: "Resistencia física",
                icono: "fas fa-tachometer-alt",
                items: [
                    "Correr, nadar o ciclismo progresivo",
                    "Sesiones de intervalos de alta intensidad",
                    "Control de respiración y ritmo cardíaco",
                    "Entrenamiento cruzado",
                    "Recuperación activa entre sesiones"
                ]
            }
        ];
        
        // Inicialización
        document.addEventListener('DOMContentLoaded', function() {
            // Cargar beneficios
            cargarBeneficios();
            
            // Cargar rutinas
            cargarRutinas();
            
            // Actualizar contadores
            actualizarContadores();
            
            // Renderizar datos existentes
            renderPacientes();
            renderIMC();
            
            // Configurar eventos
            document.getElementById('guardarPacienteBtn').addEventListener('click', guardarPaciente);
            document.getElementById('calcularIMCBtn').addEventListener('click', guardarIMC);
            
            // Permitir guardar con Enter
            document.getElementById('pnombre').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') guardarPaciente();
            });
            
            document.getElementById('inombre').addEventListener('keypress', function(e) {
                if (e.key === 'Enter') guardarIMC();
            });
            
            // Autocompletar pacientes en IMC
            document.getElementById('inombre').addEventListener('input', function() {
                mostrarSugerenciasPacientes(this.value);
            });
        });
        
        // Funciones para pacientes
        function guardarPaciente() {
            const nombre = document.getElementById('pnombre').value.trim();
            const edad = document.getElementById('pedad').value.trim();
            const meta = document.getElementById('pmeta').value.trim();
            
            if (!nombre || !edad || !meta) {
                mostrarMensaje('Por favor completa todos los campos', 'error');
                return;
            }
            
            const paciente = {
                id: Date.now(),
                nombre,
                edad: parseInt(edad),
                meta,
                fechaRegistro: new Date().toLocaleDateString()
            };
            
            if (editPacienteIndex >= 0) {
                pacientes[editPacienteIndex] = paciente;
                mostrarMensaje('Paciente actualizado correctamente', 'success');
                editPacienteIndex = -1;
                document.getElementById('guardarPacienteBtn').innerHTML = '<i class="fas fa-save"></i> Guardar paciente';
            } else {
                pacientes.push(paciente);
                mostrarMensaje('Paciente guardado correctamente', 'success');
            }
            
            // Limpiar formulario
            document.getElementById('pnombre').value = '';
            document.getElementById('pedad').value = '';
            document.getElementById('pmeta').value = '';
            
            // Actualizar datos
            guardarEnLocalStorage();
            renderPacientes();
            actualizarContadores();
        }
        
        function renderPacientes() {
            const tbody = document.getElementById('pacientesTabla');
            tbody.innerHTML = '';
            
            if (pacientes.length === 0) {
                tbody.innerHTML = `
                    <tr>
                        <td colspan="4" style="text-align: center; padding: 2rem; color: var(--texto-claro);">
                            <i class="fas fa-users" style="font-size: 2rem; margin-bottom: 1rem; display: block;"></i>
                            No hay pacientes registrados
                        </td>
                    </tr>
                `;
                return;
            }
            
            pacientes.forEach((paciente, index) => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td><strong>${paciente.nombre}</strong></td>
                    <td>${paciente.edad} años</td>
                    <td>${paciente.meta}</td>
                    <td>
                        <div class="action-buttons">
                            <button class="btn-action btn-edit" onclick="editarPaciente(${index})">
                                <i class="fas fa-edit"></i> Editar
                            </button>
                            <button class="btn-action btn-delete" onclick="eliminarPaciente(${index})">
                                <i class="fas fa-trash"></i> Eliminar
                            </button>
                        </div>
                    </td>
                `;
                tbody.appendChild(tr);
            });
        }
        
        function editarPaciente(index) {
            const paciente = pacientes[index];
            document.getElementById('pnombre').value = paciente.nombre;
            document.getElementById('pedad').value = paciente.edad;
            document.getElementById('pmeta').value = paciente.meta;
            editPacienteIndex = index;
            
            document.getElementById('guardarPacienteBtn').innerHTML = '<i class="fas fa-save"></i> Actualizar paciente';
            mostrarMensaje(`Editando paciente: ${paciente.nombre}`, 'warning');
            
            // Scroll al formulario
            document.getElementById('pnombre').focus();
        }
        
        function eliminarPaciente(index) {
            if (confirm(`¿Estás seguro de eliminar a ${pacientes[index].nombre}?`)) {
                pacientes.splice(index, 1);
                guardarEnLocalStorage();
                renderPacientes();
                actualizarContadores();
                mostrarMensaje('Paciente eliminado', 'success');
            }
        }
        
        // Funciones para IMC
        function guardarIMC() {
            const nombre = document.getElementById('inombre').value.trim();
            const peso = parseFloat(document.getElementById('ipeso').value);
            const altura = parseFloat(document.getElementById('ialtura').value);
            
            if (!nombre || !peso || !altura) {
                mostrarMensaje('Por favor completa todos los campos', 'error');
                return;
            }
            
            if (altura <= 0 || peso <= 0) {
                mostrarMensaje('Peso y altura deben ser valores positivos', 'error');
                return;
            }
            
            const imc = (peso / (altura * altura)).toFixed(2);
            const estado = calcularEstadoIMC(imc);
            const recomendacion = generarRecomendacion(estado);
            
            const registroIMC = {
                id: Date.now(),
                nombre,
                imc,
                estado: estado.texto,
                clase: estado.clase,
                recomendacion,
                peso,
                altura,
                fecha: new Date().toLocaleDateString()
            };
            
            if (editImcIndex >= 0) {
                imcs[editImcIndex] = registroIMC;
                mostrarMensaje('Evaluación actualizada correctamente', 'success');
                editImcIndex = -1;
                document.getElementById('calcularIMCBtn').innerHTML = '<i class="fas fa-calculator"></i> Calcular y guardar';
            } else {
                imcs.push(registroIMC);
                mostrarMensaje('Evaluación guardada correctamente', 'success');
            }
            
            // Limpiar formulario
            document.getElementById('inombre').value = '';
            document.getElementById('ipeso').value = '';
            document.getElementById('ialtura').value = '';
            document.getElementById('pacientesList').innerHTML = '';
            
            // Actualizar datos
            guardarEnLocalStorage();
            renderIMC();
            actualizarContadores();
            actualizarEstadisticas();
        }
        
        function calcularEstadoIMC(imc) {
            if (imc < 18.5) {
                return { texto: "Bajo peso", clase: "bajo" };
            } else if (imc < 25) {
                return { texto: "Normal", clase: "normal" };
            } else if (imc < 30) {
                return { texto: "Sobrepeso", clase: "sobrepeso" };
            } else {
                return { texto: "Obesidad", clase: "sobrepeso" };
            }
        }
        
        function generarRecomendacion(estado) {
            switch(estado.texto) {
                case "Bajo peso":
                    return "Aumentar calorías con alimentos nutritivos y entrenamiento de fuerza";
                case "Normal":
                    return "Mantener hábitos saludables y actividad física regular";
                case "Sobrepeso":
                    return "Reducir azúcares y grasas, aumentar actividad cardiovascular";
                case "Obesidad":
                    return "Consultar con especialista, dieta controlada y ejercicio supervisado";
                default:
                    return "Consulta con un profesional de la salud";
            }
        }
        
        function renderIMC() {
            const tbody = document.getElementById('imcTabla');
            tbody.innerHTML = '';
            
            if (imcs.length === 0) {
                tbody.innerHTML = `
                    <tr>
                        <td colspan="5" style="text-align: center; padding: 2rem; color: var(--texto-claro);">
                            <i class="fas fa-weight" style="font-size: 2rem; margin-bottom: 1rem; display: block;"></i>
                            No hay evaluaciones de IMC registradas
                        </td>
                    </tr>
                `;
                return;
            }
            
            imcs.forEach((registro, index) => {
                const tr = document.createElement('tr');
                tr.innerHTML = `
                    <td><strong>${registro.nombre}</strong><br><small style="color: var(--texto-claro);">${registro.fecha}</small></td>
                    <td><strong style="font-size: 1.2rem;">${registro.imc}</strong></td>
                    <td><span class="badge badge-${registro.clase}">${registro.estado}</span></td>
                    <td style="max-width: 200px;">${registro.recomendacion}</td>
                    <td>
                        <div class="action-buttons">
                            <button class="btn-action btn-edit" onclick="editarIMC(${index})">
                                <i class="fas fa-edit"></i> Editar
                            </button>
                            <button class="btn-action btn-delete" onclick="eliminarIMC(${index})">
                                <i class="fas fa-trash"></i> Eliminar
                            </button>
                        </div>
                    </td>
                `;
                tbody.appendChild(tr);
            });
        }
        
        function editarIMC(index) {
            const registro = imcs[index];
            document.getElementById('inombre').value = registro.nombre;
            document.getElementById('ipeso').value = registro.peso;
            document.getElementById('ialtura').value = registro.altura;
            editImcIndex = index;
            
            document.getElementById('calcularIMCBtn').innerHTML = '<i class="fas fa-save"></i> Actualizar evaluación';
            mostrarMensaje(`Editando evaluación de: ${registro.nombre}`, 'warning');
            
            // Scroll al formulario
            document.getElementById('inombre').focus();
        }
        
        function eliminarIMC(index) {
            if (confirm(`¿Estás seguro de eliminar esta evaluación?`)) {
                imcs.splice(index, 1);
                guardarEnLocalStorage();
                renderIMC();
                actualizarContadores();
                actualizarEstadisticas();
                mostrarMensaje('Evaluación eliminada', 'success');
            }
        }
        
        // Funciones auxiliares
        function mostrarSugerenciasPacientes(busqueda) {
            const container = document.getElementById('pacientesList');
            
            if (busqueda.length < 2) {
                container.innerHTML = '';
                return;
            }
            
            const sugerencias = pacientes.filter(p => 
                p.nombre.toLowerCase().includes(busqueda.toLowerCase())
            );
            
            if (sugerencias.length === 0) {
                container.innerHTML = '';
                return;
            }
            
            let html = '<div class="sugerencias-container">';
            sugerencias.forEach(paciente => {
                html += `
                    <div class="sugerencia-item" onclick="seleccionarPaciente('${paciente.nombre}')">
                        ${paciente.nombre} (${paciente.edad} años) - ${paciente.meta}
                    </div>
                `;
            });
            html += '</div>';
            
            container.innerHTML = html;
            
            // Estilos para las sugerencias
            const style = document.createElement('style');
            style.textContent = `
                .sugerencias-container {
                    position: absolute;
                    background: white;
                    border: 1px solid var(--borde);
                    border-radius: 10px;
                    box-shadow: var(--sombra);
                    z-index: 100;
                    width: 100%;
                    max-height: 200px;
                    overflow-y: auto;
                }
                .sugerencia-item {
                    padding: 0.8rem 1rem;
                    cursor: pointer;
                    transition: var(--transition);
                    border-bottom: 1px solid var(--borde);
                }
                .sugerencia-item:hover {
                    background-color: var(--verde-claro);
                }
                .sugerencia-item:last-child {
                    border-bottom: none;
                }
            `;
            document.head.appendChild(style);
        }
        
        function seleccionarPaciente(nombre) {
            document.getElementById('inombre').value = nombre;
            document.getElementById('pacientesList').innerHTML = '';
            document.getElementById('ipeso').focus();
        }
        
        function cargarBeneficios() {
            const container = document.querySelector('.benefits-list');
            beneficios.forEach((beneficio, index) => {
                const div = document.createElement('div');
                div.className = 'benefit-item';
                div.innerHTML = `
                    <span class="benefit-number">${index + 1}</span>
                    ${beneficio}
                `;
                container.appendChild(div);
            });
        }
        
        function cargarRutinas() {
            const container = document.getElementById('rutinasContainer');
            rutinas.forEach(rutina => {
                const div = document.createElement('div');
                div.className = 'routine';
                div.innerHTML = `
                    <div class="routine-title">
                        <i class="${rutina.icono}"></i>
                        ${rutina.titulo}
                    </div>
                    <ul class="routine-list">
                        ${rutina.items.map(item => `<li>${item}</li>`).join('')}
                    </ul>
                `;
                container.appendChild(div);
            });
        }
        
        function actualizarContadores() {
            document.getElementById('pacientesCount').textContent = `${pacientes.length} ${pacientes.length === 1 ? 'paciente' : 'pacientes'}`;
            document.getElementById('imcCount').textContent = `${imcs.length} ${imcs.length === 1 ? 'evaluación' : 'evaluaciones'}`;
        }
        
        function actualizarEstadisticas() {
            if (imcs.length === 0) {
                document.getElementById('avgIMC').textContent = '0.0';
                document.getElementById('normalCount').textContent = '0';
                document.getElementById('alertaCount').textContent = '0';
                return;
            }
            
            // IMC promedio
            const totalIMC = imcs.reduce((sum, registro) => sum + parseFloat(registro.imc), 0);
            const promedio = (totalIMC / imcs.length).toFixed(1);
            document.getElementById('avgIMC').textContent = promedio;
            
            // Conteo de normales
            const normales = imcs.filter(r => r.estado === "Normal").length;
            document.getElementById('normalCount').textContent = normales;
            
            // Conteo de alertas (no normales)
            const alertas = imcs.filter(r => r.estado !== "Normal").length;
            document.getElementById('alertaCount').textContent = alertas;
        }
        
        function mostrarMensaje(texto, tipo) {
            const container = document.getElementById('messageContainer');
            
            // Crear mensaje
            const mensaje = document.createElement('div');
            mensaje.className = `message message-${tipo}`;
            mensaje.innerHTML = `
                <i class="fas fa-${tipo === 'success' ? 'check-circle' : tipo === 'error' ? 'exclamation-circle' : 'info-circle'}"></i>
                <span>${texto}</span>
            `;
            
            // Agregar al contenedor
            container.appendChild(mensaje);
            
            // Mostrar con animación
            setTimeout(() => {
                mensaje.classList.add('show');
            }, 10);
            
            // Remover después de 5 segundos
            setTimeout(() => {
                mensaje.classList.remove('show');
                setTimeout(() => {
                    if (container.contains(mensaje)) {
                        container.removeChild(mensaje);
                    }
                }, 500);
            }, 5000);
        }
        
        function guardarEnLocalStorage() {
            localStorage.setItem('nutri-pacientes', JSON.stringify(pacientes));
            localStorage.setItem('nutri-imcs', JSON.stringify(imcs));
        }
    </script>
</body>
</html>
