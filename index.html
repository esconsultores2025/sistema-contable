<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sistema Contable - Base de Datos Compartida</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8fafc;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            background: linear-gradient(135deg, #1e3a8a, #3b82f6);
            color: white;
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .connection-status {
            position: fixed;
            top: 70px;
            right: 20px;
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 12px;
            font-weight: bold;
            z-index: 1001;
        }

        .status-connected {
            background: #10b981;
            color: white;
        }

        .status-disconnected {
            background: #ef4444;
            color: white;
        }

        .user-selector {
            background: white;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.07);
            display: flex;
            align-items: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .supervisor-badge {
            background: linear-gradient(135deg, #dc2626, #ef4444);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-weight: bold;
            font-size: 12px;
            text-transform: uppercase;
        }

        .card {
            background: white;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.07);
            padding: 25px;
            margin-bottom: 25px;
            border: 1px solid #e2e8f0;
        }

        .tabs {
            display: flex;
            background: #f1f5f9;
            border-radius: 12px;
            margin-bottom: 25px;
            overflow: hidden;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
            flex-wrap: wrap;
        }

        .tab {
            flex: 1;
            padding: 15px 20px;
            background: none;
            border: none;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s ease;
            color: #64748b;
            min-width: 150px;
        }

        .tab.active {
            background: #3b82f6;
            color: white;
            transform: translateY(-2px);
        }

        .tab.supervisor-tab {
            background: #dc2626;
            color: white;
        }

        .tab.supervisor-tab.active {
            background: #991b1b;
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
        }

        .form-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: #374151;
            font-size: 14px;
        }

        input, select, textarea {
            width: 100%;
            padding: 12px 16px;
            border: 2px solid #e5e7eb;
            border-radius: 8px;
            font-size: 14px;
            transition: all 0.3s ease;
            background: #fff;
        }

        input:focus, select:focus, textarea:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 3px rgba(59, 130, 246, 0.1);
        }

        .btn {
            background: #3b82f6;
            color: white;
            border: none;
            padding: 12px 24px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-right: 10px;
            margin-bottom: 10px;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn:hover {
            background: #2563eb;
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(59, 130, 246, 0.3);
        }

        .btn.danger {
            background: #ef4444;
        }

        .btn.danger:hover {
            background: #dc2626;
        }

        .btn.success {
            background: #10b981;
        }

        .btn.success:hover {
            background: #059669;
        }

        .btn.warning {
            background: #f59e0b;
        }

        .btn.warning:hover {
            background: #d97706;
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-bottom: 25px;
        }

        .stat-card {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 20px;
            border-radius: 12px;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, rgba(255,255,255,0.1), rgba(255,255,255,0));
            pointer-events: none;
        }

        .stat-number {
            font-size: 32px;
            font-weight: bold;
            margin-bottom: 5px;
            position: relative;
        }

        .stat-label {
            font-size: 14px;
            opacity: 0.9;
            position: relative;
        }

        .efficiency-comparison {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-bottom: 25px;
        }

        .assistant-card {
            background: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.07);
            border-left: 5px solid #3b82f6;
            position: relative;
        }

        .assistant-card.excellent {
            border-left-color: #10b981;
        }

        .assistant-card.good {
            border-left-color: #3b82f6;
        }

        .assistant-card.warning {
            border-left-color: #f59e0b;
        }

        .assistant-card.poor {
            border-left-color: #ef4444;
        }

        .assistant-card.online::after {
            content: '🟢';
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 12px;
        }

        .assistant-card.offline::after {
            content: '🔴';
            position: absolute;
            top: 10px;
            right: 10px;
            font-size: 12px;
        }

        .efficiency-bar {
            width: 100%;
            height: 20px;
            background: #e5e7eb;
            border-radius: 10px;
            overflow: hidden;
            margin: 10px 0;
        }

        .efficiency-fill {
            height: 100%;
            transition: width 0.3s ease;
            border-radius: 10px;
        }

        .efficiency-excellent {
            background: #10b981;
        }

        .efficiency-good {
            background: #3b82f6;
        }

        .efficiency-warning {
            background: #f59e0b;
        }

        .efficiency-poor {
            background: #ef4444;
        }

        .alert {
            padding: 15px;
            margin: 10px 0;
            border-radius: 8px;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .alert-success {
            background: #d1fae5;
            color: #065f46;
            border: 1px solid #a7f3d0;
        }

        .alert-warning {
            background: #fef3c7;
            color: #92400e;
            border: 1px solid #fcd34d;
        }

        .alert-danger {
            background: #fee2e2;
            color: #991b1b;
            border: 1px solid #fca5a5;
        }

        .alert-info {
            background: #dbeafe;
            color: #1e40af;
            border: 1px solid #93c5fd;
        }

        .current-time {
            position: fixed;
            top: 20px;
            right: 20px;
            background: rgba(59, 130, 246, 0.95);
            color: white;
            padding: 12px 20px;
            border-radius: 10px;
            font-weight: bold;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
            z-index: 1000;
        }

        .live-activity {
            background: #f0fdf4;
            border: 2px solid #10b981;
            border-radius: 10px;
            padding: 15px;
            margin-bottom: 15px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 0 0 rgba(16, 185, 129, 0.4); }
            70% { box-shadow: 0 0 0 10px rgba(16, 185, 129, 0); }
            100% { box-shadow: 0 0 0 0 rgba(16, 185, 129, 0); }
        }

        .blinking {
            animation: blink 1s infinite;
        }

        @keyframes blink {
            0%, 50% { opacity: 1; }
            51%, 100% { opacity: 0.3; }
        }

        .timer-display {
            font-size: 24px;
            font-weight: bold;
            color: #1e40af;
            text-align: center;
            padding: 20px;
            background: #eff6ff;
            border-radius: 10px;
            margin: 20px 0;
        }

        .client-list, .process-list, .pending-list {
            max-height: 400px;
            overflow-y: auto;
        }

        .client-item, .process-item, .pending-item {
            background: #f8fafc;
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 10px;
            border-left: 4px solid #3b82f6;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .process-item {
            border-left-color: #10b981;
        }

        .pending-item {
            border-left-color: #f59e0b;
        }

        .priority-high {
            border-left-color: #ef4444 !important;
            background: #fef2f2;
        }

        .priority-medium {
            border-left-color: #f59e0b !important;
            background: #fffbeb;
        }

        .priority-low {
            border-left-color: #10b981 !important;
            background: #f0fdf4;
        }

        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
        }

        .modal-content {
            background-color: white;
            margin: 5% auto;
            padding: 30px;
            border-radius: 15px;
            width: 90%;
            max-width: 800px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            max-height: 80vh;
            overflow-y: auto;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
            line-height: 1;
        }

        .close:hover {
            color: #333;
        }

        .real-time-indicator {
            display: inline-block;
            width: 10px;
            height: 10px;
            background: #10b981;
            border-radius: 50%;
            margin-right: 8px;
            animation: pulse 1s infinite;
        }

        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            
            .tabs {
                flex-direction: column;
            }
            
            .form-grid {
                grid-template-columns: 1fr;
            }
            
            .stats-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .efficiency-comparison {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <div class="current-time" id="currentTime"></div>
    <div class="connection-status" id="connectionStatus">🔴 Desconectado</div>
    
    <div class="container">
        <div class="header">
            <h1>Sistema Contable - Base de Datos Compartida</h1>
            <p>Control en Tiempo Real de Todo el Equipo</p>
            <div style="margin-top: 10px;">
                <span class="real-time-indicator"></span>
                <small>Sincronización en tiempo real activa</small>
            </div>
        </div>

        <div class="user-selector">
            <label><strong>Usuario Actual:</strong></label>
            <select id="usuarioActual" onchange="cambiarUsuario()">
                <option value="">Seleccionar Usuario</option>
                <option value="supervisor">👨‍💼 CONTADOR GENERAL (Supervisor)</option>
            </select>
            <button class="btn" onclick="mostrarModalUsuario()">➕ Nuevo Asistente</button>
            <div id="supervisorBadge" class="supervisor-badge" style="display: none;">MODO SUPERVISOR</div>
        </div>

        <div class="tabs" id="mainTabs">
            <!-- Tabs se generan dinámicamente -->
        </div>

        <!-- Dashboard -->
        <div id="dashboard" class="tab-content active">
            <div class="stats-grid">
                <div class="stat-card">
                    <div class="stat-number" id="totalClientes">0</div>
                    <div class="stat-label">Clientes Asignados</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="procesosHoy">0</div>
                    <div class="stat-label">Procesos Hoy</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="pendientesActivos">0</div>
                    <div class="stat-label">Pendientes Activos</div>
                </div>
                <div class="stat-card">
                    <div class="stat-number" id="eficienciaGeneral">0%</div>
                    <div class="stat-label">Eficiencia General</div>
                </div>
            </div>

            <div class="card">
                <h3>Resumen de Actividades del Día</h3>
                <div id="resumenDia"></div>
            </div>
        </div>

        <!-- Panel Supervisor -->
        <div id="supervisor" class="tab-content">
            <div class="card">
                <h2>🎯 Panel de Control en Tiempo Real</h2>
                
                <!-- Actividad en Tiempo Real -->
                <div class="card">
                    <h3><span class="real-time-indicator"></span>Actividad en Tiempo Real</h3>
                    <div id="actividadTiempoReal"></div>
                </div>
                
                <!-- Alertas de Retrasos -->
                <div id="alertasRetrasos"></div>
                
                <!-- Comparación de Eficiencias -->
                <h3>📊 Comparación de Eficiencias</h3>
                <div class="efficiency-comparison" id="comparacionEficiencias"></div>
            </div>

            <!-- Reporte Diario en Tiempo Real -->
            <div class="card">
                <h2>📈 Reporte Diario en Tiempo Real</h2>
                <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 20px;">
                    <input type="date" id="fechaReporteDiario" onchange="actualizarReporteTiempoReal()">
                    <button class="btn success" onclick="exportarReporteTiempoReal()">📊 Exportar</button>
                </div>
                <div id="reporteTiempoReal"></div>
            </div>

            <!-- Monitoreo Individual -->
            <div class="card">
                <h2>👤 Monitoreo Individual Detallado</h2>
                <div class="form-group">
                    <label>Seleccionar Asistente:</label>
                    <select id="asistenteMonitoreo" onchange="actualizarMonitoreoIndividual()">
                        <option value="">Todos los asistentes</option>
                    </select>
                </div>
                <div id="monitoreoIndividual"></div>
            </div>
        </div>

        <!-- Clientes -->
        <div id="clientes" class="tab-content">
            <div class="card">
                <h2>Gestión de Cartera de Clientes</h2>
                <div class="form-grid">
                    <div class="form-group">
                        <label>Nombre del Cliente:</label>
                        <input type="text" id="nombreCliente" placeholder="Ej: Empresa ABC S.A.C.">
                    </div>
                    <div class="form-group">
                        <label>RUC:</label>
                        <input type="text" id="rucCliente" placeholder="20123456789">
                    </div>
                    <div class="form-group">
                        <label>Tipo de Régimen:</label>
                        <select id="regimenCliente">
                            <option value="General">Régimen General</option>
                            <option value="MYPE">Régimen MYPE Tributario</option>
                            <option value="Especial">Régimen Especial</option>
                            <option value="RUS">Régimen Único Simplificado</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Contacto:</label>
                        <input type="text" id="contactoCliente" placeholder="Teléfono / Email">
                    </div>
                </div>
                <button class="btn success" onclick="agregarCliente()">Agregar Cliente</button>
                
                <div class="client-list" id="listaClientes"></div>
            </div>
        </div>

        <!-- Procesos -->
        <div id="procesos" class="tab-content">
            <div class="card">
                <h2>Procesos Contables Estándar</h2>
                <div class="form-grid">
                    <div class="form-group">
                        <label>Nombre del Proceso:</label>
                        <input type="text" id="nombreProceso" placeholder="Ej: Declaración IGV Mensual">
                    </div>
                    <div class="form-group">
                        <label>Tiempo Estándar (horas):</label>
                        <input type="number" id="tiempoEstandar" step="0.5" min="0.5" placeholder="2.5">
                    </div>
                    <div class="form-group">
                        <label>Frecuencia:</label>
                        <select id="frecuenciaProceso">
                            <option value="Mensual">Mensual</option>
                            <option value="Bimensual">Bimensual</option>
                            <option value="Trimestral">Trimestral</option>
                            <option value="Anual">Anual</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Día de Vencimiento:</label>
                        <input type="number" id="diaVencimiento" min="1" max="31" placeholder="12">
                    </div>
                </div>
                <button class="btn success" onclick="agregarProceso()">Agregar Proceso</button>
                
                <div class="process-list" id="listaProcesos"></div>
            </div>

            <div class="card">
                <h2>Asignar Proceso a Cliente</h2>
                <div class="form-grid">
                    <div class="form-group">
                        <label>Cliente:</label>
                        <select id="clienteProceso">
                            <option value="">Seleccionar cliente</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Proceso:</label>
                        <select id="procesoAsignar">
                            <option value="">Seleccionar proceso</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Mes/Periodo:</label>
                        <input type="month" id="periodoAsignacion">
                    </div>
                </div>
                <button class="btn" onclick="asignarProcesoCliente()">Asignar Proceso</button>
                
                <div id="procesosAsignados"></div>
            </div>
        </div>

        <!-- Pendientes -->
        <div id="pendientes" class="tab-content">
            <div class="card">
                <h2>Lista de Pendientes</h2>
                <div class="form-grid">
                    <div class="form-group">
                        <label>Descripción del Pendiente:</label>
                        <textarea id="descripcionPendiente" rows="3" placeholder="Describir el pendiente..."></textarea>
                    </div>
                    <div class="form-group">
                        <label>Cliente Relacionado:</label>
                        <select id="clientePendiente">
                            <option value="">Sin cliente específico</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Prioridad:</label>
                        <select id="prioridadPendiente">
                            <option value="Alta">Alta</option>
                            <option value="Media">Media</option>
                            <option value="Baja">Baja</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label>Fecha Límite:</label>
                        <input type="date" id="fechaLimite">
                    </div>
                </div>
                <button class="btn success" onclick="agregarPendiente()">Agregar Pendiente</button>
                
                <div class="pending-list" id="listaPendientes"></div>
            </div>
        </div>

        <!-- Control de Tiempo -->
        <div id="tiempo" class="tab-content">
            <div class="card">
                <h2>Control de Tiempo de Procesos</h2>
                <div class="form-grid">
                    <div class="form-group">
                        <label>Proceso Asignado:</label>
                        <select id="procesoTiempo">
                            <option value="">Seleccionar proceso</option>
                        </select>
                    </div>
                </div>
                
                <div class="timer-display" id="cronometro">00:00:00</div>
                
                <div style="text-align: center;">
                    <button class="btn success" id="btnIniciar" onclick="iniciarCronometro()">▶️ Iniciar</button>
                    <button class="btn warning" id="btnPausar" onclick="pausarCronometro()" disabled>⏸️ Pausar</button>
                    <button class="btn danger" id="btnDetener" onclick="detenerCronometro()" disabled>⏹️ Finalizar</button>
                </div>

                <div id="procesoActual" style="margin-top: 20px;"></div>
            </div>

            <div class="card">
                <h2>Historial de Tiempos</h2>
                <div id="historialTiempos"></div>
            </div>
        </div>
    </div>

    <!-- Modal para nuevo usuario -->
    <div id="modalUsuario" class="modal">
        <div class="modal-content">
            <span class="close" onclick="cerrarModalUsuario()">&times;</span>
            <h2>Crear Nuevo Asistente</h2>
            <div class="form-group">
                <label>Nombre Completo:</label>
                <input type="text" id="nombreUsuario" placeholder="Ej: María González">
            </div>
            <div class="form-group">
                <label>Cargo:</label>
                <select id="cargoUsuario">
                    <option value="Asistente Jr.">Asistente Contable Jr.</option>
                    <option value="Asistente Sr.">Asistente Contable Sr.</option>
                    <option value="Auxiliar">Auxiliar Contable</option>
                </select>
            </div>
            <button class="btn success" onclick="crearUsuario()">Crear Asistente</button>
        </div>
    </div>

    <script>
        // =================== BASE DE DATOS COMPARTIDA ===================
        
        // Simulación de base de datos compartida usando localStorage
        // En producción esto sería una base de datos real (Firebase, MySQL, etc.)
        
        class BaseDatosCompartida {
            constructor() {
                this.prefijo = 'sistema_contable_';
                this.listeners = new Map();
                this.sincronizando = false;
                this.inicializarSincronizacion();
            }
            
            // Simular conexión a base de datos
            inicializarSincronizacion() {
                this.actualizarEstadoConexion(true);
                
                // Simular sincronización cada 5 segundos
                setInterval(() => {
                    this.sincronizarDatos();
                }, 5000);
                
                // Escuchar cambios en localStorage (para simular tiempo real)
                window.addEventListener('storage', (e) => {
                    if (e.key && e.key.startsWith(this.prefijo)) {
                        this.notificarCambio(e.key, e.newValue);
                    }
                });
            
            // Resumen general
            eficienciaGeneral = contadorEficiencia > 0 ? eficienciaGeneral / contadorEficiencia : 0;
            
            reporteHTML = `
                <div class="stats-grid" style="margin-bottom: 20px;">
                    <div class="stat-card">
                        <div class="stat-number">${totalProcesos}</div>
                        <div class="stat-label">Total Procesos</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">${totalHoras.toFixed(1)}h</div>
                        <div class="stat-label">Total Horas</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">${eficienciaGeneral.toFixed(1)}%</div>
                        <div class="stat-label">Eficiencia General</div>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">${usuarios.filter(u => {
                            const ultimaActividad = new Date(u.ultimaActividad || 0);
                            const ahora = new Date();
                            const minutosInactivo = (ahora - ultimaActividad) / 60000;
                            return minutosInactivo < 10;
                        }).length}</div>
                        <div class="stat-label">Asistentes Online</div>
                    </div>
                </div>
            ` + reporteHTML;
            
            container.innerHTML = reporteHTML;
        }
        
        function actualizarMonitoreoIndividual() {
            const asistenteId = document.getElementById('asistenteMonitoreo')?.value;
            const container = document.getElementById('monitoreoIndividual');
            if (!container) return;
            
            if (!asistenteId) {
                // Mostrar resumen de todos
                container.innerHTML = `
                    <div class="alert alert-info">
                        Seleccione un asistente específico para ver detalles individuales, o vea el resumen general arriba.
                    </div>
                `;
                return;
            }
            
            const usuario = usuarios.find(u => u.id === asistenteId);
            if (!usuario) return;
            
            const registros = registrosTiempo[asistenteId] || [];
            const clientesUsuario = clientes[asistenteId] || [];
            const pendientesUsuario = pendientes[asistenteId] || [];
            const actividadUsuario = actividadTiempoReal[asistenteId] || [];
            
            const hoy = new Date().toDateString();
            const registrosHoy = registros.filter(r => new Date(r.fecha).toDateString() === hoy);
            const pendientesActivos = pendientesUsuario.filter(p => p.estado === 'pendiente');
            
            container.innerHTML = `
                <div class="card">
                    <h3>📋 Detalle Individual - ${usuario.nombre}</h3>
                    
                    <div class="stats-grid" style="margin-bottom: 20px;">
                        <div class="stat-card">
                            <div class="stat-number">${clientesUsuario.length}</div>
                            <div class="stat-label">Clientes Asignados</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-number">${registrosHoy.length}</div>
                            <div class="stat-label">Procesos Hoy</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-number">${pendientesActivos.length}</div>
                            <div class="stat-label">Pendientes Activos</div>
                        </div>
                        <div class="stat-card">
                            <div class="stat-number">${registros.length > 0 ? 
                                (registros.reduce((sum, r) => sum + r.eficiencia, 0) / registros.length).toFixed(1) : 0}%</div>
                            <div class="stat-label">Eficiencia Promedio</div>
                        </div>
                    </div>
                    
                    <h4>📊 Actividad Reciente</h4>
                    <div style="max-height: 300px; overflow-y: auto;">
                        ${actividadUsuario.slice(-10).reverse().map(actividad => `
                            <div class="alert alert-info" style="margin: 5px 0;">
                                <div style="display: flex; justify-content: space-between;">
                                    <span>${actividad.descripcion}</span>
                                    <small>${obtenerTiempoTranscurrido(actividad.timestamp)}</small>
                                </div>
                            </div>
                        `).join('')}
                    </div>
                    
                    <h4>📝 Pendientes Activos</h4>
                    <div style="max-height: 200px; overflow-y: auto;">
                        ${pendientesActivos.map(pendiente => {
                            const cliente = clientesUsuario.find(c => c.id === pendiente.clienteId);
                            return `
                                <div class="pending-item priority-${pendiente.prioridad.toLowerCase()}">
                                    <div>
                                        <strong>${pendiente.descripcion}</strong><br>
                                        <small>Cliente: ${cliente?.nombre || 'General'} | Prioridad: ${pendiente.prioridad}</small>
                                    </div>
                                </div>
                            `;
                        }).join('')}
                    </div>
                </div>
            `;
        }
        
        function exportarReporteTiempoReal() {
            const fecha = document.getElementById('fechaReporteDiario').value;
            
            let csvContent = "data:text/csv;charset=utf-8,";
            csvContent += "Fecha,Asistente,Cargo,Estado,Procesos_Completados,Horas_Trabajadas,Eficiencia_Promedio,Ultima_Actividad\n";
            
            const fechaObj = new Date(fecha);
            const fechaStr = fechaObj.toDateString();
            
            usuarios.forEach(usuario => {
                const registros = registrosTiempo[usuario.id] || [];
                const registrosFecha = registros.filter(r => new Date(r.fecha).toDateString() === fechaStr);
                
                const procesosUsuario = registrosFecha.length;
                const horasUsuario = registrosFecha.reduce((sum, r) => sum + r.tiempoReal, 0);
                const eficienciaUsuario = registrosFecha.length > 0 ? 
                    registrosFecha.reduce((sum, r) => sum + r.eficiencia, 0) / registrosFecha.length : 0;
                
                const ultimaActividad = new Date(usuario.ultimaActividad || 0);
                const ahora = new Date();
                const minutosInactivo = (ahora - ultimaActividad) / 60000;
                const estado = minutosInactivo < 10 ? 'Online' : 'Offline';
                
                csvContent += `${fecha},${usuario.nombre},${usuario.cargo},${estado},${procesosUsuario},${horasUsuario.toFixed(2)},${eficienciaUsuario.toFixed(2)},${usuario.ultimaActividad}\n`;
            });
            
            const encodedUri = encodeURI(csvContent);
            const link = document.createElement("a");
            link.setAttribute("href", encodedUri);
            link.setAttribute("download", `reporte_tiempo_real_${fecha}.csv`);
            document.body.appendChild(link);
            link.click();
            document.body.removeChild(link);
            
            mostrarAlerta('Reporte en tiempo real exportado exitosamente', 'success');
        }
        
        // =================== GESTIÓN DE DATOS ===================
        
        function agregarCliente() {
            if (!usuarioActual || usuarioActual === 'supervisor') {
                alert('Seleccione un asistente primero');
                return;
            }
            
            const nombre = document.getElementById('nombreCliente').value.trim();
            const ruc = document.getElementById('rucCliente').value.trim();
            const regimen = document.getElementById('regimenCliente').value;
            const contacto = document.getElementById('contactoCliente').value.trim();
            
            if (!nombre || !ruc) {
                alert('Complete los campos obligatorios');
                return;
            }
            
            const cliente = {
                id: Date.now().toString(),
                nombre: nombre,
                ruc: ruc,
                regimen: regimen,
                contacto: contacto,
                fechaAsignacion: new Date().toISOString()
            };
            
            if (!clientes[usuarioActual]) {
                clientes[usuarioActual] = [];
            }
            
            clientes[usuarioActual].push(cliente);
            bd.guardar('clientes', clientes);
            
            // Registrar actividad
            bd.registrarActividad(usuarioActual, {
                tipo: 'cliente_agregado',
                descripcion: `Agregó nuevo cliente: ${nombre}`,
                datos: { clienteId: cliente.id, nombre: nombre }
            });
            
            // Limpiar formulario
            document.getElementById('nombreCliente').value = '';
            document.getElementById('rucCliente').value = '';
            document.getElementById('contactoCliente').value = '';
            
            actualizarListaClientes();
            actualizarTodosLosSelects();
            mostrarAlerta('Cliente agregado exitosamente', 'success');
        }
        
        function agregarProceso() {
            const nombre = document.getElementById('nombreProceso').value.trim();
            const tiempo = parseFloat(document.getElementById('tiempoEstandar').value);
            const frecuencia = document.getElementById('frecuenciaProceso').value;
            const diaVencimiento = parseInt(document.getElementById('diaVencimiento').value);
            
            if (!nombre || !tiempo || !diaVencimiento) {
                alert('Complete todos los campos');
                return;
            }
            
            const proceso = {
                id: Date.now().toString(),
                nombre: nombre,
                tiempoEstandar: tiempo,
                frecuencia: frecuencia,
                diaVencimiento: diaVencimiento
            };
            
            procesos.push(proceso);
            bd.guardar('procesos', procesos);
            
            // Limpiar formulario
            document.getElementById('nombreProceso').value = '';
            document.getElementById('tiempoEstandar').value = '';
            document.getElementById('diaVencimiento').value = '';
            
            actualizarListaProcesos();
            actualizarTodosLosSelects();
            mostrarAlerta('Proceso agregado exitosamente', 'success');
        }
        
        function asignarProcesoCliente() {
            if (!usuarioActual || usuarioActual === 'supervisor') {
                alert('Seleccione un asistente primero');
                return;
            }
            
            const clienteId = document.getElementById('clienteProceso').value;
            const procesoId = document.getElementById('procesoAsignar').value;
            const periodo = document.getElementById('periodoAsignacion').value;
            
            if (!clienteId || !procesoId || !periodo) {
                alert('Complete todos los campos');
                return;
            }
            
            const asignacion = {
                id: Date.now().toString(),
                clienteId: clienteId,
                procesoId: procesoId,
                periodo: periodo,
                estado: 'pendiente',
                fechaAsignacion: new Date().toISOString()
            };
            
            if (!procesosAsignados[usuarioActual]) {
                procesosAsignados[usuarioActual] = [];
            }
            
            procesosAsignados[usuarioActual].push(asignacion);
            bd.guardar('procesosAsignados', procesosAsignados);
            
            // Registrar actividad
            const cliente = clientes[usuarioActual]?.find(c => c.id === clienteId);
            const proceso = procesos.find(p => p.id === procesoId);
            
            bd.registrarActividad(usuarioActual, {
                tipo: 'proceso_asignado',
                descripcion: `Asignó proceso ${proceso?.nombre} a cliente ${cliente?.nombre} para ${periodo}`,
                datos: { clienteId, procesoId, periodo }
            });
            
            actualizarProcesosAsignados();
            actualizarTodosLosSelects();
            mostrarAlerta('Proceso asignado exitosamente', 'success');
        }
        
        function agregarPendiente() {
            if (!usuarioActual || usuarioActual === 'supervisor') {
                alert('Seleccione un asistente primero');
                return;
            }
            
            const descripcion = document.getElementById('descripcionPendiente').value.trim();
            const clienteId = document.getElementById('clientePendiente').value;
            const prioridad = document.getElementById('prioridadPendiente').value;
            const fechaLimite = document.getElementById('fechaLimite').value;
            
            if (!descripcion) {
                alert('Ingrese la descripción del pendiente');
                return;
            }
            
            const pendiente = {
                id: Date.now().toString(),
                descripcion: descripcion,
                clienteId: clienteId,
                prioridad: prioridad,
                fechaLimite: fechaLimite,
                estado: 'pendiente',
                fechaCreacion: new Date().toISOString()
            };
            
            if (!pendientes[usuarioActual]) {
                pendientes[usuarioActual] = [];
            }
            
            pendientes[usuarioActual].push(pendiente);
            bd.guardar('pendientes', pendientes);
            
            // Registrar actividad
            bd.registrarActividad(usuarioActual, {
                tipo: 'pendiente_agregado',
                descripcion: `Agregó pendiente: ${descripcion}`,
                datos: { pendienteId: pendiente.id, prioridad: prioridad }
            });
            
            // Limpiar formulario
            document.getElementById('descripcionPendiente').value = '';
            document.getElementById('clientePendiente').value = '';
            
            actualizarListaPendientes();
            mostrarAlerta('Pendiente agregado exitosamente', 'success');
        }
        
        // =================== CONTROL DE TIEMPO ===================
        
        function iniciarCronometro() {
            const procesoId = document.getElementById('procesoTiempo').value;
            if (!procesoId) {
                alert('Seleccione un proceso');
                return;
            }
            
            cronometroActivo = true;
            cronometroInicio = Date.now() - cronometroPausado;
            procesoEnCurso = procesoId;
            
            document.getElementById('btnIniciar').disabled = true;
            document.getElementById('btnPausar').disabled = false;
            document.getElementById('btnDetener').disabled = false;
            
            mostrarProcesoActual();
            
            // Registrar actividad de inicio
            const asignacion = procesosAsignados[usuarioActual]?.find(a => a.procesoId === procesoEnCurso);
            const proceso = procesos.find(p => p.id === procesoEnCurso);
            const cliente = clientes[usuarioActual]?.find(c => c.id === asignacion?.clienteId);
            
            if (proceso && cliente) {
                bd.registrarActividad(usuarioActual, {
                    tipo: 'proceso_iniciado',
                    descripcion: `Inició proceso ${proceso.nombre} para cliente ${cliente.nombre}`,
                    datos: { procesoId, clienteId: cliente.id }
                });
            }
        }
        
        function pausarCronometro() {
            cronometroActivo = false;
            cronometroPausado = Date.now() - cronometroInicio;
            
            document.getElementById('btnIniciar').disabled = false;
            document.getElementById('btnPausar').disabled = true;
            
            // Registrar actividad de pausa
            bd.registrarActividad(usuarioActual, {
                tipo: 'proceso_pausado',
                descripcion: `Pausó el cronómetro del proceso en curso`,
                datos: { procesoId: procesoEnCurso }
            });
        }
        
        function detenerCronometro() {
            if (!procesoEnCurso) return;
            
            const tiempoTotal = Math.round((Date.now() - cronometroInicio) / 1000);
            const horas = tiempoTotal / 3600;
            
            // Buscar la asignación correspondiente
            const asignacion = procesosAsignados[usuarioActual]?.find(a => a.procesoId === procesoEnCurso);
            const proceso = procesos.find(p => p.id === procesoEnCurso);
            
            if (asignacion && proceso) {
                const registro = {
                    id: Date.now().toString(),
                    asignacionId: asignacion.id,
                    procesoId: procesoEnCurso,
                    clienteId: asignacion.clienteId,
                    tiempoReal: horas,
                    tiempoEstandar: proceso.tiempoEstandar,
                    eficiencia: (proceso.tiempoEstandar / horas) * 100,
                    fecha: new Date().toISOString(),
                    estado: 'completado'
                };
                
                if (!registrosTiempo[usuarioActual]) {
                    registrosTiempo[usuarioActual] = [];
                }
                
                registrosTiempo[usuarioActual].push(registro);
                bd.guardar('registrosTiempo', registrosTiempo);
                
                // Marcar asignación como completada
                asignacion.estado = 'completado';
                asignacion.fechaCompletado = new Date().toISOString();
                bd.guardar('procesosAsignados', procesosAsignados);
                
                // Registrar actividad de finalización
                const cliente = clientes[usuarioActual]?.find(c => c.id === asignacion.clienteId);
                bd.registrarActividad(usuarioActual, {
                    tipo: 'proceso_completado',
                    descripcion: `Completó proceso ${proceso.nombre} para cliente ${cliente?.nombre} (${registro.eficiencia.toFixed(1)}% eficiencia)`,
                    datos: { 
                        procesoId: procesoEnCurso, 
                        clienteId: asignacion.clienteId,
                        eficiencia: registro.eficiencia,
                        tiempoReal: horas,
                        tiempoEstandar: proceso.tiempoEstandar
                    }
                });
            }
            
            // Resetear cronómetro
            cronometroActivo = false;
            cronometroInicio = null;
            cronometroPausado = 0;
            procesoEnCurso = null;
            
            document.getElementById('btnIniciar').disabled = false;
            document.getElementById('btnPausar').disabled = true;
            document.getElementById('btnDetener').disabled = true;
            document.getElementById('cronometro').textContent = '00:00:00';
            document.getElementById('procesoActual').innerHTML = '';
            
            actualizarHistorialTiempos();
            actualizarProcesosAsignados();
            mostrarAlerta('Proceso completado y registrado', 'success');
        }
        
        function mostrarProcesoActual() {
            if (!procesoEnCurso) return;
            
            const asignacion = procesosAsignados[usuarioActual]?.find(a => a.procesoId === procesoEnCurso);
            const proceso = procesos.find(p => p.id === procesoEnCurso);
            const cliente = clientes[usuarioActual]?.find(c => c.id === asignacion?.clienteId);
            
            if (asignacion && proceso && cliente) {
                document.getElementById('procesoActual').innerHTML = `
                    <div class="alert alert-success">
                        <strong>Proceso en curso:</strong> ${proceso.nombre}<br>
                        <strong>Cliente:</strong> ${cliente.nombre}<br>
                        <strong>Tiempo estándar:</strong> ${proceso.tiempoEstandar} horas<br>
                        <strong>Periodo:</strong> ${asignacion.periodo}
                    </div>
                `;
            }
        }
        
        // =================== FUNCIONES DE ACTUALIZACIÓN ===================
        
        function actualizarTodosLosSelects() {
            if (!usuarioActual || usuarioActual === 'supervisor') return;
            
            // Actualizar select de clientes
            const selectsClientes = ['clienteProceso', 'clientePendiente'];
            selectsClientes.forEach(selectId => {
                const select = document.getElementById(selectId);
                if (!select) return;
                select.innerHTML = '<option value="">Seleccionar cliente</option>';
                
                if (clientes[usuarioActual]) {
                    clientes[usuarioActual].forEach(cliente => {
                        const option = document.createElement('option');
                        option.value = cliente.id;
                        option.textContent = cliente.nombre;
                        select.appendChild(option);
                    });
                }
            });
            
            // Actualizar select de procesos
            const selectProcesos = document.getElementById('procesoAsignar');
            if (selectProcesos) {
                selectProcesos.innerHTML = '<option value="">Seleccionar proceso</option>';
                
                procesos.forEach(proceso => {
                    const option = document.createElement('option');
                    option.value = proceso.id;
                    option.textContent = `${proceso.nombre} (${proceso.tiempoEstandar}h)`;
                    selectProcesos.appendChild(option);
                });
            }
            
            // Actualizar select de procesos para tiempo
            const selectTiempo = document.getElementById('procesoTiempo');
            if (selectTiempo) {
                selectTiempo.innerHTML = '<option value="">Seleccionar proceso</option>';
                
                if (procesosAsignados[usuarioActual]) {
                    procesosAsignados[usuarioActual]
                        .filter(asignacion => asignacion.estado === 'pendiente')
                        .forEach(asignacion => {
                            const proceso = procesos.find(p => p.id === asignacion.procesoId);
                            const cliente = clientes[usuarioActual]?.find(c => c.id === asignacion.clienteId);
                            
                            if (proceso && cliente) {
                                const option = document.createElement('option');
                                option.value = proceso.id;
                                option.textContent = `${proceso.nombre} - ${cliente.nombre} (${asignacion.periodo})`;
                                selectTiempo.appendChild(option);
                            }
                        });
                }
            }
        }
        
        function actualizarTodasLasListas() {
            actualizarListaClientes();
            actualizarListaProcesos();
            actualizarListaPendientes();
            actualizarProcesosAsignados();
            actualizarHistorialTiempos();
        }
        
        function actualizarListaClientes() {
            const lista = document.getElementById('listaClientes');
            if (!lista) return;
            lista.innerHTML = '';
            
            if (!usuarioActual || usuarioActual === 'supervisor' || !clientes[usuarioActual]) return;
            
            clientes[usuarioActual].forEach(cliente => {
                const div = document.createElement('div');
                div.className = 'client-item';
                div.innerHTML = `
                    <div>
                        <h4>${cliente.nombre}</h4>
                        <p><strong>RUC:</strong> ${cliente.ruc} | <strong>Régimen:</strong> ${cliente.regimen}</p>
                        <p><strong>Contacto:</strong> ${cliente.contacto}</p>
                    </div>
                    <button class="btn danger" onclick="eliminarCliente('${cliente.id}')">🗑️ Eliminar</button>
                `;
                lista.appendChild(div);
            });
        }
        
        function actualizarListaProcesos() {
            const lista = document.getElementById('listaProcesos');
            if (!lista) return;
            lista.innerHTML = '';
            
            procesos.forEach(proceso => {
                const div = document.createElement('div');
                div.className = 'process-item';
                div.innerHTML = `
                    <div>
                        <h4>${proceso.nombre}</h4>
                        <p><strong>Tiempo estándar:</strong> ${proceso.tiempoEstandar} horas</p>
                        <p><strong>Frecuencia:</strong> ${proceso.frecuencia} | <strong>Vence día:</strong> ${proceso.diaVencimiento}</p>
                    </div>
                    <button class="btn danger" onclick="eliminarProceso('${proceso.id}')">🗑️ Eliminar</button>
                `;
                lista.appendChild(div);
            });
        }
        
        function actualizarListaPendientes() {
            const lista = document.getElementById('listaPendientes');
            if (!lista) return;
            lista.innerHTML = '';
            
            if (!usuarioActual || usuarioActual === 'supervisor' || !pendientes[usuarioActual]) return;
            
            pendientes[usuarioActual]
                .filter(pendiente => pendiente.estado === 'pendiente')
                .sort((a, b) => {
                    const prioridadOrden = { 'Alta': 3, 'Media': 2, 'Baja': 1 };
                    return prioridadOrden[b.prioridad] - prioridadOrden[a.prioridad];
                })
                .forEach(pendiente => {
                    const cliente = clientes[usuarioActual]?.find(c => c.id === pendiente.clienteId);
                    const clienteNombre = cliente ? cliente.nombre : 'General';
                    
                    const div = document.createElement('div');
                    div.className = `pending-item priority-${pendiente.prioridad.toLowerCase()}`;
                    div.innerHTML = `
                        <div>
                            <h4>${pendiente.descripcion}</h4>
                            <p><strong>Cliente:</strong> ${clienteNombre} | <strong>Prioridad:</strong> ${pendiente.prioridad}</p>
                            <p><strong>Fecha límite:</strong> ${pendiente.fechaLimite || 'Sin fecha'}</p>
                        </div>
                        <div>
                            <button class="btn success" onclick="completarPendiente('${pendiente.id}')">✅ Completar</button>
                            <button class="btn danger" onclick="eliminarPendiente('${pendiente.id}')">🗑️ Eliminar</button>
                        </div>
                    `;
                    lista.appendChild(div);
                });
        }
        
        function actualizarProcesosAsignados() {
            const lista = document.getElementById('procesosAsignados');
            if (!lista) return;
            lista.innerHTML = '<h3>Procesos Asignados</h3>';
            
            if (!usuarioActual || usuarioActual === 'supervisor' || !procesosAsignados[usuarioActual]) return;
            
            procesosAsignados[usuarioActual].forEach(asignacion => {
                const proceso = procesos.find(p => p.id === asignacion.procesoId);
                const cliente = clientes[usuarioActual]?.find(c => c.id === asignacion.clienteId);
                
                if (proceso && cliente) {
                    const estadoClass = asignacion.estado === 'completado' ? 'success' : 'warning';
                    const estadoTexto = asignacion.estado === 'completado' ? 'Completado' : 'Pendiente';
                    
                    const div = document.createElement('div');
                    div.className = `process-item`;
                    div.innerHTML = `
                        <div>
                            <h4>${proceso.nombre} - ${cliente.nombre}</h4>
                            <p><strong>Periodo:</strong> ${asignacion.periodo} | <strong>Estado:</strong> 
                            <span class="alert alert-${estadoClass}" style="display: inline; padding: 2px 8px; font-size: 12px;">${estadoTexto}</span></p>
                            <p><strong>Tiempo estándar:</strong> ${proceso.tiempoEstandar} horas</p>
                        </div>
                    `;
                    lista.appendChild(div);
                }
            });
        }
        
        function actualizarHistorialTiempos() {
            const lista = document.getElementById('historialTiempos');
            if (!lista) return;
            lista.innerHTML = '';
            
            if (!usuarioActual || usuarioActual === 'supervisor' || !registrosTiempo[usuarioActual]) return;
            
            registrosTiempo[usuarioActual]
                .sort((a, b) => new Date(b.fecha) - new Date(a.fecha))
                .slice(0, 10)
                .forEach(registro => {
                    const proceso = procesos.find(p => p.id === registro.procesoId);
                    const cliente = clientes[usuarioActual]?.find(c => c.id === registro.clienteId);
                    
                    if (proceso && cliente) {
                        const eficienciaClass = registro.eficiencia >= 100 ? 'excellent' : 
                                              registro.eficiencia >= 80 ? 'good' : 
                                              registro.eficiencia >= 60 ? 'warning' : 'poor';
                        
                        const div = document.createElement('div');
                        div.className = 'process-item';
                        div.innerHTML = `
                            <div>
                                <h4>${proceso.nombre} - ${cliente.nombre}</h4>
                                <p><strong>Fecha:</strong> ${new Date(registro.fecha).toLocaleDateString('es-PE')}</p>
                                <p><strong>Tiempo real:</strong> ${registro.tiempoReal.toFixed(2)}h | 
                                   <strong>Tiempo estándar:</strong> ${registro.tiempoEstandar}h</p>
                                <div class="efficiency-meter">
                                    <span>Eficiencia:</span>
                                    <div class="efficiency-bar">
                                        <div class="efficiency-fill efficiency-${eficienciaClass}" 
                                             style="width: ${Math.min(registro.eficiencia, 100)}%"></div>
                                    </div>
                                    <span>${registro.eficiencia.toFixed(1)}%</span>
                                </div>
                            </div>
                        `;
                        lista.appendChild(div);
                    }
                });
        }
        
        function actualizarDashboard() {
            if (!usuarioActual || usuarioActual === 'supervisor') return;
            
            // Total clientes
            const totalClientes = clientes[usuarioActual]?.length || 0;
            document.getElementById('totalClientes').textContent = totalClientes;
            
            // Procesos hoy
            const hoy = new Date().toISOString().split('T')[0];
            const procesosHoy = registrosTiempo[usuarioActual]?.filter(r => 
                r.fecha.split('T')[0] === hoy
            ).length || 0;
            document.getElementById('procesosHoy').textContent = procesosHoy;
            
            // Pendientes activos
            const pendientesActivos = pendientes[usuarioActual]?.filter(p => 
                p.estado === 'pendiente'
            ).length || 0;
            document.getElementById('pendientesActivos').textContent = pendientesActivos;
            
            // Eficiencia general
            const registros = registrosTiempo[usuarioActual] || [];
            const eficienciaPromedio = registros.length > 0 ? 
                registros.reduce((sum, r) => sum + r.eficiencia, 0) / registros.length : 0;
            document.getElementById('eficienciaGeneral').textContent = `${eficienciaPromedio.toFixed(1)}%`;
        }
        
        // =================== FUNCIONES DE ELIMINACIÓN ===================
        
        function eliminarCliente(id) {
            if (confirm('¿Está seguro de eliminar este cliente?')) {
                const cliente = clientes[usuarioActual].find(c => c.id === id);
                clientes[usuarioActual] = clientes[usuarioActual].filter(c => c.id !== id);
                bd.guardar('clientes', clientes);
                
                // Registrar actividad
                bd.registrarActividad(usuarioActual, {
                    tipo: 'cliente_eliminado',
                    descripcion: `Eliminó cliente: ${cliente?.nombre}`,
                    datos: { clienteId: id }
                });
                
                actualizarListaClientes();
                actualizarTodosLosSelects();
            }
        }
        
        function eliminarProceso(id) {
            if (confirm('¿Está seguro de eliminar este proceso?')) {
                const proceso = procesos.find(p => p.id === id);
                procesos = procesos.filter(p => p.id !== id);
                bd.guardar('procesos', procesos);
                
                actualizarListaProcesos();
                actualizarTodosLosSelects();
            }
        }
        
        function completarPendiente(id) {
            const pendiente = pendientes[usuarioActual].find(p => p.id === id);
            if (pendiente) {
                pendiente.estado = 'completado';
                pendiente.fechaCompletado = new Date().toISOString();
                bd.guardar('pendientes', pendientes);
                
                // Registrar actividad
                bd.registrarActividad(usuarioActual, {
                    tipo: 'pendiente_completado',
                    descripcion: `Completó pendiente: ${pendiente.descripcion}`,
                    datos: { pendienteId: id }
                });
                
                actualizarListaPendientes();
                mostrarAlerta('Pendiente completado', 'success');
            }
        }
        
        function eliminarPendiente(id) {
            if (confirm('¿Está seguro de eliminar este pendiente?')) {
                const pendiente = pendientes[usuarioActual].find(p => p.id === id);
                pendientes[usuarioActual] = pendientes[usuarioActual].filter(p => p.id !== id);
                bd.guardar('pendientes', pendientes);
                
                // Registrar actividad
                bd.registrarActividad(usuarioActual, {
                    tipo: 'pendiente_eliminado',
                    descripcion: `Eliminó pendiente: ${pendiente?.descripcion}`,
                    datos: { pendienteId: id }
                });
                
                actualizarListaPendientes();
            }
        }
        
        // =================== UTILIDADES ===================
        
        function mostrarAlerta(mensaje, tipo) {
            const alertaExistente = document.querySelector('.alerta-temporal');
            if (alertaExistente) {
                alertaExistente.remove();
            }
            
            const alerta = document.createElement('div');
            alerta.className = `alert alert-${tipo} alerta-temporal`;
            alerta.style.position = 'fixed';
            alerta.style.top = '120px';
            alerta.style.right = '20px';
            alerta.style.zIndex = '9999';
            alerta.style.minWidth = '300px';
            alerta.textContent = mensaje;
            
            document.body.appendChild(alerta);
            
            setTimeout(() => {
                alerta.remove();
            }, 3000);
        }
        
        // Cerrar modal al hacer clic fuera
        window.onclick = function(event) {
            const modal = document.getElementById('modalUsuario');
            if (event.target === modal) {
                cerrarModalUsuario();
            }
        }
    </script>
</body>
</html>
            }
            
            // Obtener datos de la "base de datos"
            obtener(clave) {
                try {
                    const data = localStorage.getItem(this.prefijo + clave);
                    return data ? JSON.parse(data) : null;
                } catch (error) {
                    console.error('Error al obtener datos:', error);
                    return null;
                }
            }
            
            // Guardar datos en la "base de datos"
            guardar(clave, datos) {
                try {
                    const dataString = JSON.stringify(datos);
                    localStorage.setItem(this.prefijo + clave, dataString);
                    
                    // Notificar cambio a todos los listeners
                    this.notificarCambio(this.prefijo + clave, dataString);
                    
                    // Simular envío a servidor
                    this.enviarAlServidor(clave, datos);
                    
                    return true;
                } catch (error) {
                    console.error('Error al guardar datos:', error);
                    return false;
                }
            }
            
            // Simular envío al servidor
            enviarAlServidor(clave, datos) {
                // En producción aquí haría una llamada real al servidor
                console.log(`📡 Sincronizando ${clave} con servidor...`);
                
                // Simular latencia de red
                setTimeout(() => {
                    this.mostrarNotificacionSincronizacion(`Datos de ${clave} sincronizados`);
                }, Math.random() * 1000);
            }
            
            // Obtener todos los datos de todos los usuarios
            obtenerTodosDatos() {
                const datos = {
                    usuarios: this.obtener('usuarios') || [],
                    clientes: this.obtener('clientes') || {},
                    procesos: this.obtener('procesos') || [],
                    procesosAsignados: this.obtener('procesosAsignados') || {},
                    pendientes: this.obtener('pendientes') || {},
                    registrosTiempo: this.obtener('registrosTiempo') || {},
                    actividadTiempoReal: this.obtener('actividadTiempoReal') || {}
                };
                
                return datos;
            }
            
            // Registrar actividad en tiempo real
            registrarActividad(usuarioId, actividad) {
                const actividades = this.obtener('actividadTiempoReal') || {};
                
                if (!actividades[usuarioId]) {
                    actividades[usuarioId] = [];
                }
                
                const nuevaActividad = {
                    id: Date.now().toString(),
                    tipo: actividad.tipo,
                    descripcion: actividad.descripcion,
                    timestamp: new Date().toISOString(),
                    datos: actividad.datos || {}
                };
                
                actividades[usuarioId].push(nuevaActividad);
                
                // Mantener solo las últimas 50 actividades por usuario
                if (actividades[usuarioId].length > 50) {
                    actividades[usuarioId] = actividades[usuarioId].slice(-50);
                }
                
                this.guardar('actividadTiempoReal', actividades);
            }
            
            // Escuchar cambios en tiempo real
            escucharCambios(clave, callback) {
                if (!this.listeners.has(clave)) {
                    this.listeners.set(clave, []);
                }
                this.listeners.get(clave).push(callback);
            }
            
            // Notificar cambios a los listeners
            notificarCambio(clave, nuevoValor) {
                const claveSimple = clave.replace(this.prefijo, '');
                const listeners = this.listeners.get(claveSimple);
                
                if (listeners) {
                    const datos = nuevoValor ? JSON.parse(nuevoValor) : null;
                    listeners.forEach(callback => {
                        try {
                            callback(datos);
                        } catch (error) {
                            console.error('Error en callback:', error);
                        }
                    });
                }
            }
            
            // Simular sincronización de datos
            sincronizarDatos() {
                if (this.sincronizando) return;
                
                this.sincronizando = true;
                
                // Simular verificación de cambios del servidor
                setTimeout(() => {
                    this.sincronizando = false;
                    // Aquí se actualizarían los datos desde el servidor
                }, 500);
            }
            
            // Actualizar estado de conexión
            actualizarEstadoConexion(conectado) {
                const status = document.getElementById('connectionStatus');
                if (status) {
                    if (conectado) {
                        status.textContent = '🟢 Conectado';
                        status.className = 'connection-status status-connected';
                    } else {
                        status.textContent = '🔴 Desconectado';
                        status.className = 'connection-status status-disconnected';
                    }
                }
            }
            
            // Mostrar notificación de sincronización
            mostrarNotificacionSincronizacion(mensaje) {
                // En una versión más avanzada mostraría notificaciones toast
                console.log(`✅ ${mensaje}`);
            }
        }
        
        // =================== VARIABLES GLOBALES ===================
        
        const bd = new BaseDatosCompartida();
        let usuarioActual = localStorage.getItem('usuarioActual') || '';
        
        // Variables de datos
        let usuarios = [];
        let clientes = {};
        let procesos = [];
        let procesosAsignados = {};
        let pendientes = {};
        let registrosTiempo = {};
        let actividadTiempoReal = {};
        
        // Variables de cronómetro
        let cronometroActivo = false;
        let cronometroInicio = null;
        let cronometroPausado = 0;
        let procesoEnCurso = null;
        
        // =================== INICIALIZACIÓN ===================
        
        document.addEventListener('DOMContentLoaded', function() {
            inicializarSistema();
        });
        
        function inicializarSistema() {
            // Configurar intervalos
            actualizarHora();
            setInterval(actualizarHora, 1000);
            setInterval(actualizarCronometro, 1000);
            
            // Cargar datos desde la base de datos compartida
            cargarDatosDesdeBD();
            
            // Configurar listeners de tiempo real
            configurarListenersTiempoReal();
            
            // Configurar interfaz
            cargarUsuarios();
            generarTabs();
            
            if (usuarioActual) {
                document.getElementById('usuarioActual').value = usuarioActual;
                cambiarUsuario();
            }
            
            // Establecer fechas por defecto
            const hoy = new Date().toISOString().split('T')[0];
            document.getElementById('fechaLimite').value = hoy;
            document.getElementById('periodoAsignacion').value = new Date().toISOString().slice(0, 7);
            document.getElementById('fechaReporteDiario').value = hoy;
            
            // Simular datos iniciales si no existen
            if (usuarios.length === 0) {
                crearDatosIniciales();
            }
        }
        
        function cargarDatosDesdeBD() {
            const datos = bd.obtenerTodosDatos();
            
            usuarios = datos.usuarios;
            clientes = datos.clientes;
            procesos = datos.procesos;
            procesosAsignados = datos.procesosAsignados;
            pendientes = datos.pendientes;
            registrosTiempo = datos.registrosTiempo;
            actividadTiempoReal = datos.actividadTiempoReal;
        }
        
        function configurarListenersTiempoReal() {
            // Escuchar cambios en tiempo real
            bd.escucharCambios('actividadTiempoReal', (nuevaActividad) => {
                actividadTiempoReal = nuevaActividad || {};
                if (usuarioActual === 'supervisor') {
                    actualizarActividadTiempoReal();
                }
            });
            
            bd.escucharCambios('registrosTiempo', (nuevosRegistros) => {
                registrosTiempo = nuevosRegistros || {};
                if (usuarioActual === 'supervisor') {
                    actualizarPanelSupervisor();
                }
            });
            
            bd.escucharCambios('usuarios', (nuevosUsuarios) => {
                usuarios = nuevosUsuarios || [];
                cargarUsuarios();
                if (usuarioActual === 'supervisor') {
                    actualizarPanelSupervisor();
                }
            });
        }
        
        function crearDatosIniciales() {
            // Crear usuarios de ejemplo
            const usuariosEjemplo = [
                {
                    id: 'user1',
                    nombre: 'María González',
                    cargo: 'Asistente Sr.',
                    fechaCreacion: new Date().toISOString(),
                    ultimaActividad: new Date().toISOString(),
                    estado: 'online'
                },
                {
                    id: 'user2', 
                    nombre: 'Juan Pérez',
                    cargo: 'Asistente Jr.',
                    fechaCreacion: new Date().toISOString(),
                    ultimaActividad: new Date(Date.now() - 300000).toISOString(), // 5 min ago
                    estado: 'online'
                },
                {
                    id: 'user3',
                    nombre: 'Ana López',
                    cargo: 'Auxiliar',
                    fechaCreacion: new Date().toISOString(),
                    ultimaActividad: new Date(Date.now() - 600000).toISOString(), // 10 min ago
                    estado: 'offline'
                }
            ];
            
            // Procesos de ejemplo
            const procesosEjemplo = [
                {
                    id: 'proc1',
                    nombre: 'Declaración IGV Mensual',
                    tiempoEstandar: 2.5,
                    frecuencia: 'Mensual',
                    diaVencimiento: 12
                },
                {
                    id: 'proc2',
                    nombre: 'Declaración Renta Anual',
                    tiempoEstandar: 8,
                    frecuencia: 'Anual',
                    diaVencimiento: 31
                },
                {
                    id: 'proc3',
                    nombre: 'Libros Contables',
                    tiempoEstandar: 4,
                    frecuencia: 'Mensual',
                    diaVencimiento: 15
                }
            ];
            
            // Registros de tiempo de ejemplo
            const registrosEjemplo = {
                'user1': [
                    {
                        id: 'reg1',
                        procesoId: 'proc1',
                        clienteId: 'cli1',
                        tiempoReal: 2.2,
                        tiempoEstandar: 2.5,
                        eficiencia: 113.6,
                        fecha: new Date().toISOString(),
                        estado: 'completado'
                    }
                ],
                'user2': [
                    {
                        id: 'reg2',
                        procesoId: 'proc2',
                        clienteId: 'cli2',
                        tiempoReal: 3.1,
                        tiempoEstandar: 2.5,
                        eficiencia: 80.6,
                        fecha: new Date().toISOString(),
                        estado: 'completado'
                    }
                ]
            };
            
            // Actividad de ejemplo
            const actividadEjemplo = {
                'user1': [
                    {
                        id: 'act1',
                        tipo: 'proceso_iniciado',
                        descripcion: 'Inició proceso de Declaración IGV para Cliente ABC',
                        timestamp: new Date(Date.now() - 1800000).toISOString(), // 30 min ago
                        datos: { procesoId: 'proc1', clienteId: 'cli1' }
                    },
                    {
                        id: 'act2',
                        tipo: 'proceso_completado',
                        descripcion: 'Completó Declaración IGV para Cliente ABC',
                        timestamp: new Date(Date.now() - 600000).toISOString(), // 10 min ago
                        datos: { procesoId: 'proc1', clienteId: 'cli1', eficiencia: 113.6 }
                    }
                ],
                'user2': [
                    {
                        id: 'act3',
                        tipo: 'login',
                        descripcion: 'Se conectó al sistema',
                        timestamp: new Date(Date.now() - 3600000).toISOString(), // 1 hour ago
                        datos: {}
                    }
                ]
            };
            
            // Guardar en base de datos
            bd.guardar('usuarios', usuariosEjemplo);
            bd.guardar('procesos', procesosEjemplo);
            bd.guardar('registrosTiempo', registrosEjemplo);
            bd.guardar('actividadTiempoReal', actividadEjemplo);
            
            // Recargar datos
            cargarDatosDesdeBD();
        }
        
        // =================== FUNCIONES DE TIEMPO ===================
        
        function actualizarHora() {
            const ahora = new Date();
            document.getElementById('currentTime').textContent = ahora.toLocaleString('es-PE');
        }
        
        function actualizarCronometro() {
            if (cronometroActivo && cronometroInicio) {
                const tiempoTranscurrido = Date.now() - cronometroInicio;
                const horas = Math.floor(tiempoTranscurrido / 3600000);
                const minutos = Math.floor((tiempoTranscurrido % 3600000) / 60000);
                const segundos = Math.floor((tiempoTranscurrido % 60000) / 1000);
                
                document.getElementById('cronometro').textContent = 
                    `${horas.toString().padStart(2, '0')}:${minutos.toString().padStart(2, '0')}:${segundos.toString().padStart(2, '0')}`;
            }
        }
        
        // =================== FUNCIONES DE INTERFAZ ===================
        
        function generarTabs() {
            const tabsContainer = document.getElementById('mainTabs');
            const esSupervisor = usuarioActual === 'supervisor';
            
            const tabsNormales = [
                {id: 'dashboard', label: '📊 Dashboard'},
                {id: 'clientes', label: '👥 Clientes'},
                {id: 'procesos', label: '⚙️ Procesos'},
                {id: 'pendientes', label: '📝 Pendientes'},
                {id: 'tiempo', label: '⏱️ Control Tiempo'}
            ];

            const tabsSupervisor = [
                {id: 'supervisor', label: '🎯 PANEL SUPERVISOR', class: 'supervisor-tab'},
                {id: 'procesos', label: '⚙️ Procesos Globales'}
            ];

            const tabs = esSupervisor ? tabsSupervisor : tabsNormales;
            
            tabsContainer.innerHTML = tabs.map(tab => 
                `<button class="tab ${tab.class || ''}" onclick="showTab('${tab.id}')">${tab.label}</button>`
            ).join('');
            
            // Activar primera tab
            const firstTab = tabs[0];
            showTab(firstTab.id);
        }
        
        function showTab(tabName) {
            const tabs = document.querySelectorAll('.tab-content');
            tabs.forEach(tab => tab.classList.remove('active'));
            
            const tabButtons = document.querySelectorAll('.tab');
            tabButtons.forEach(btn => btn.classList.remove('active'));
            
            document.getElementById(tabName).classList.add('active');
            event.target.classList.add('active');
            
            if (tabName === 'dashboard') {
                actualizarDashboard();
            } else if (tabName === 'supervisor') {
                actualizarPanelSupervisor();
            }
        }
        
        // =================== GESTIÓN DE USUARIOS ===================
        
        function mostrarModalUsuario() {
            document.getElementById('modalUsuario').style.display = 'block';
        }

        function cerrarModalUsuario() {
            document.getElementById('modalUsuario').style.display = 'none';
            document.getElementById('nombreUsuario').value = '';
        }

        function crearUsuario() {
            const nombre = document.getElementById('nombreUsuario').value.trim();
            const cargo = document.getElementById('cargoUsuario').value;
            
            if (!nombre) {
                alert('Por favor ingrese el nombre del asistente');
                return;
            }
            
            const usuario = {
                id: Date.now().toString(),
                nombre: nombre,
                cargo: cargo,
                fechaCreacion: new Date().toISOString(),
                ultimaActividad: new Date().toISOString(),
                estado: 'online'
            };
            
            usuarios.push(usuario);
            bd.guardar('usuarios', usuarios);
            
            // Inicializar datos para el nuevo usuario
            clientes[usuario.id] = [];
            pendientes[usuario.id] = [];
            registrosTiempo[usuario.id] = [];
            procesosAsignados[usuario.id] = [];
            
            bd.guardar('clientes', clientes);
            bd.guardar('pendientes', pendientes);
            bd.guardar('registrosTiempo', registrosTiempo);
            bd.guardar('procesosAsignados', procesosAsignados);
            
            // Registrar actividad
            bd.registrarActividad(usuario.id, {
                tipo: 'usuario_creado',
                descripcion: `Nuevo asistente registrado: ${nombre}`
            });
            
            cargarUsuarios();
            cerrarModalUsuario();
            
            // Seleccionar automáticamente el nuevo usuario
            document.getElementById('usuarioActual').value = usuario.id;
            cambiarUsuario();
            
            mostrarAlerta('Usuario creado exitosamente', 'success');
        }

        function cargarUsuarios() {
            const select = document.getElementById('usuarioActual');
            const currentValue = select.value;
            
            select.innerHTML = '<option value="">Seleccionar Usuario</option>';
            
            // Agregar opción de supervisor
            const optionSupervisor = document.createElement('option');
            optionSupervisor.value = 'supervisor';
            optionSupervisor.textContent = '👨‍💼 CONTADOR GENERAL (Supervisor)';
            select.appendChild(optionSupervisor);
            
            usuarios.forEach(usuario => {
                const option = document.createElement('option');
                option.value = usuario.id;
                option.textContent = `${usuario.nombre} (${usuario.cargo})`;
                select.appendChild(option);
            });
            
            // Restaurar selección
            if (currentValue) {
                select.value = currentValue;
            }
            
            // Actualizar select de monitoreo individual
            const selectMonitoreo = document.getElementById('asistenteMonitoreo');
            if (selectMonitoreo) {
                const currentMonitoreo = selectMonitoreo.value;
                selectMonitoreo.innerHTML = '<option value="">Todos los asistentes</option>';
                
                usuarios.forEach(usuario => {
                    const option = document.createElement('option');
                    option.value = usuario.id;
                    option.textContent = usuario.nombre;
                    selectMonitoreo.appendChild(option);
                });
                
                if (currentMonitoreo) {
                    selectMonitoreo.value = currentMonitoreo;
                }
            }
        }

        function cambiarUsuario() {
            usuarioActual = document.getElementById('usuarioActual').value;
            localStorage.setItem('usuarioActual', usuarioActual);
            
            const supervisorBadge = document.getElementById('supervisorBadge');
            
            if (usuarioActual === 'supervisor') {
                supervisorBadge.style.display = 'block';
            } else {
                supervisorBadge.style.display = 'none';
                
                // Registrar actividad de login
                if (usuarioActual) {
                    bd.registrarActividad(usuarioActual, {
                        tipo: 'login',
                        descripcion: 'Se conectó al sistema'
                    });
                    
                    // Actualizar estado del usuario
                    const usuario = usuarios.find(u => u.id === usuarioActual);
                    if (usuario) {
                        usuario.ultimaActividad = new Date().toISOString();
                        usuario.estado = 'online';
                        bd.guardar('usuarios', usuarios);
                    }
                }
            }
            
            generarTabs();
            
            if (usuarioActual && usuarioActual !== 'supervisor') {
                actualizarTodosLosSelects();
                actualizarTodasLasListas();
                actualizarDashboard();
            } else if (usuarioActual === 'supervisor') {
                actualizarPanelSupervisor();
            }
        }
        
        // =================== PANEL SUPERVISOR ===================
        
        function actualizarPanelSupervisor() {
            if (usuarioActual !== 'supervisor') return;
            
            actualizarActividadTiempoReal();
            verificarAlertas();
            actualizarComparacionEficiencias();
            actualizarReporteTiempoReal();
            actualizarMonitoreoIndividual();
        }
        
        function actualizarActividadTiempoReal() {
            const container = document.getElementById('actividadTiempoReal');
            if (!container) return;
            
            container.innerHTML = '';
            
            // Obtener las últimas actividades de todos los usuarios
            const todasActividades = [];
            
            Object.keys(actividadTiempoReal).forEach(usuarioId => {
                const usuario = usuarios.find(u => u.id === usuarioId);
                if (usuario && actividadTiempoReal[usuarioId]) {
                    actividadTiempoReal[usuarioId].forEach(actividad => {
                        todasActividades.push({
                            ...actividad,
                            usuario: usuario.nombre,
                            usuarioId: usuarioId
                        });
                    });
                }
            });
            
            // Ordenar por timestamp (más reciente primero)
            todasActividades.sort((a, b) => new Date(b.timestamp) - new Date(a.timestamp));
            
            // Mostrar las últimas 10 actividades
            const actividadesRecientes = todasActividades.slice(0, 10);
            
            if (actividadesRecientes.length === 0) {
                container.innerHTML = '<div class="alert alert-info">No hay actividad reciente</div>';
                return;
            }
            
            actividadesRecientes.forEach(actividad => {
                const tiempoTranscurrido = obtenerTiempoTranscurrido(actividad.timestamp);
                const esReciente = new Date() - new Date(actividad.timestamp) < 300000; // 5 minutos
                
                const div = document.createElement('div');
                div.className = esReciente ? 'live-activity' : 'alert alert-info';
                div.innerHTML = `
                    <div style="display: flex; justify-content: space-between; align-items: center;">
                        <div>
                            <strong>${actividad.usuario}</strong>: ${actividad.descripcion}
                        </div>
                        <small>${tiempoTranscurrido}</small>
                    </div>
                `;
                container.appendChild(div);
            });
        }
        
        function obtenerTiempoTranscurrido(timestamp) {
            const ahora = new Date();
            const fecha = new Date(timestamp);
            const diferencia = ahora - fecha;
            
            const minutos = Math.floor(diferencia / 60000);
            const horas = Math.floor(minutos / 60);
            const dias = Math.floor(horas / 24);
            
            if (dias > 0) return `hace ${dias} día${dias > 1 ? 's' : ''}`;
            if (horas > 0) return `hace ${horas} hora${horas > 1 ? 's' : ''}`;
            if (minutos > 0) return `hace ${minutos} minuto${minutos > 1 ? 's' : ''}`;
            return 'ahora mismo';
        }
        
        function verificarAlertas() {
            const alertasContainer = document.getElementById('alertasRetrasos');
            if (!alertasContainer) return;
            
            alertasContainer.innerHTML = '';
            
            const hoy = new Date();
            const alertas = [];
            
            // Verificar procesos retrasados
            usuarios.forEach(usuario => {
                const procesosUsuario = procesosAsignados[usuario.id] || [];
                
                procesosUsuario.forEach(asignacion => {
                    if (asignacion.estado === 'pendiente') {
                        const proceso = procesos.find(p => p.id === asignacion.procesoId);
                        const cliente = clientes[usuario.id]?.find(c => c.id === asignacion.clienteId);
                        
                        if (proceso && cliente) {
                            const [año, mes] = asignacion.periodo.split('-');
                            const fechaVencimiento = new Date(año, mes - 1, proceso.diaVencimiento);
                            
                            if (fechaVencimiento <= hoy) {
                                const diasRetraso = Math.floor((hoy - fechaVencimiento) / (1000 * 60 * 60 * 24));
                                
                                alertas.push({
                                    tipo: 'retraso',
                                    usuario: usuario.nombre,
                                    proceso: proceso.nombre,
                                    cliente: cliente.nombre,
                                    dias: diasRetraso,
                                    urgencia: diasRetraso > 5 ? 'alta' : 'media'
                                });
                            }
                        }
                    }
                });
            });
            
            // Mostrar alertas
            if (alertas.length === 0) {
                alertasContainer.innerHTML = '<div class="alert alert-success">✅ No hay procesos retrasados</div>';
            } else {
                alertas.forEach(alerta => {
                    const tipoAlerta = alerta.urgencia === 'alta' ? 'danger' : 'warning';
                    const icono = alerta.urgencia === 'alta' ? '🚨' : '⚠️';
                    const claseAnimacion = alerta.urgencia === 'alta' ? 'blinking' : '';
                    
                    alertasContainer.innerHTML += `
                        <div class="alert alert-${tipoAlerta} ${claseAnimacion}">
                            ${icono} <strong>${alerta.usuario}</strong> tiene retraso de <strong>${alerta.dias} días</strong> 
                            en proceso <strong>${alerta.proceso}</strong> del cliente <strong>${alerta.cliente}</strong>
                        </div>
                    `;
                });
            }
        }
        
        function actualizarComparacionEficiencias() {
            const container = document.getElementById('comparacionEficiencias');
            if (!container) return;
            
            container.innerHTML = '';
            
            usuarios.forEach(usuario => {
                const registros = registrosTiempo[usuario.id] || [];
                const eficienciaPromedio = registros.length > 0 ? 
                    registros.reduce((sum, r) => sum + r.eficiencia, 0) / registros.length : 0;
                
                const hoy = new Date().toDateString();
                const procesosHoy = registros.filter(r => {
                    const fechaRegistro = new Date(r.fecha).toDateString();
                    return fechaRegistro === hoy;
                }).length;
                
                const eficienciaClass = eficienciaPromedio >= 90 ? 'excellent' : 
                                      eficienciaPromedio >= 75 ? 'good' : 
                                      eficienciaPromedio >= 60 ? 'warning' : 'poor';
                
                const eficienciaFillClass = eficienciaPromedio >= 90 ? 'efficiency-excellent' : 
                                           eficienciaPromedio >= 75 ? 'efficiency-good' : 
                                           eficienciaPromedio >= 60 ? 'efficiency-warning' : 'efficiency-poor';
                
                // Determinar estado online/offline
                const ultimaActividad = new Date(usuario.ultimaActividad || 0);
                const ahora = new Date();
                const minutosInactivo = (ahora - ultimaActividad) / 60000;
                const estadoOnline = minutosInactivo < 10 ? 'online' : 'offline';
                
                container.innerHTML += `
                    <div class="assistant-card ${eficienciaClass} ${estadoOnline}">
                        <h4>${usuario.nombre}</h4>
                        <p><strong>Cargo:</strong> ${usuario.cargo}</p>
                        <p><strong>Procesos completados hoy:</strong> ${procesosHoy}</p>
                        <p><strong>Última actividad:</strong> ${obtenerTiempoTranscurrido(usuario.ultimaActividad)}</p>
                        <p><strong>Eficiencia promedio:</strong></p>
                        <div class="efficiency-bar">
                            <div class="${eficienciaFillClass} efficiency-fill" style="width: ${Math.min(eficienciaPromedio, 100)}%"></div>
                        </div>
                        <p style="text-align: center; font-weight: bold;">${eficienciaPromedio.toFixed(1)}%</p>
                    </div>
                `;
            });
        }
        
        function actualizarReporteTiempoReal() {
            const fecha = document.getElementById('fechaReporteDiario')?.value || new Date().toISOString().split('T')[0];
            const container = document.getElementById('reporteTiempoReal');
            if (!container) return;
            
            const fechaObj = new Date(fecha);
            const fechaStr = fechaObj.toDateString();
            
            let reporteHTML = `<h3>📊 Reporte en Tiempo Real - ${fechaObj.toLocaleDateString('es-PE')}</h3>`;
            
            let totalProcesos = 0;
            let totalHoras = 0;
            let eficienciaGeneral = 0;
            let contadorEficiencia = 0;
            
            usuarios.forEach(usuario => {
                const registros = registrosTiempo[usuario.id] || [];
                const registrosFecha = registros.filter(r => new Date(r.fecha).toDateString() === fechaStr);
                
                const procesosUsuario = registrosFecha.length;
                const horasUsuario = registrosFecha.reduce((sum, r) => sum + r.tiempoReal, 0);
                const eficienciaUsuario = registrosFecha.length > 0 ?
                    registrosFecha.reduce((sum, r) => sum + r.eficiencia, 0) / registrosFecha.length : 0;
                
                totalProcesos += procesosUsuario;
                totalHoras += horasUsuario;
                if (eficienciaUsuario > 0) {
                    eficienciaGeneral += eficienciaUsuario;
                    contadorEficiencia++;
                }
                
                // Determinar estado actual
                const ultimaActividad = new Date(usuario.ultimaActividad || 0);
                const ahora = new Date();
                const minutosInactivo = (ahora - ultimaActividad) / 60000;
                const estado = minutosInactivo < 10 ? '🟢 Online' : '🔴 Offline';
                
                reporteHTML += `
                    <div class="alert alert-info">
                        <div style="display: flex; justify-content: space-between; align-items: center;">
                            <div>
                                <h4>${usuario.nombre} ${estado}</h4>
                                <p><strong>Procesos:</strong> ${procesosUsuario} | <strong>Horas:</strong> ${horasUsuario.toFixed(1)}h | <strong>Eficiencia:</strong> ${eficienciaUsuario.toFixed(1)}%</p>
                            </div>
                            <div style="text-align: right;">
                                <small>Última actividad:<br>${obtenerTiempoTranscurrido(usuario.ultimaActividad)}</small>
                            </div>
                        </div>
                    </div>
                `;
            });
