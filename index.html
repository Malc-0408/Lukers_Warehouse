<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SICIT v5.0 - Sistema Lukers</title>
    
    <!-- Google API Client Library -->
    <script src="https://apis.google.com/js/api.js"></script>
    <script src="https://accounts.google.com/gsi/client" async defer></script>
    
    <!-- SheetJS para Excel -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #2563eb;
            --success: #10b981;
            --warning: #f59e0b;
            --danger: #ef4444;
            --bg-primary: #f8fafc;
            --bg-card: #ffffff;
            --text-primary: #1e293b;
            --text-secondary: #64748b;
            --border: #e2e8f0;
            --shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
        }

        [data-theme="dark"] {
            --bg-primary: #0f172a;
            --bg-card: #334155;
            --text-primary: #f1f5f9;
            --text-secondary: #94a3b8;
            --border: #475569;
        }

        body {
            font-family: 'Inter', -apple-system, sans-serif;
            background: var(--bg-primary);
            color: var(--text-primary);
        }

        .app-container {
            display: flex;
            height: 100vh;
        }

        .sidebar {
            width: 280px;
            background: linear-gradient(180deg, #1e3a8a 0%, #1e40af 100%);
            color: white;
            display: flex;
            flex-direction: column;
        }

        .sidebar-header {
            padding: 1.5rem;
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .sidebar-title {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .nav-menu {
            flex: 1;
            padding: 1rem;
            overflow-y: auto;
        }

        .nav-item {
            display: flex;
            align-items: center;
            gap: 0.75rem;
            padding: 0.875rem 1rem;
            margin-bottom: 0.5rem;
            border-radius: 0.5rem;
            cursor: pointer;
            transition: all 0.2s;
            color: rgba(255,255,255,0.8);
        }

        .nav-item:hover {
            background: rgba(255,255,255,0.1);
            color: white;
        }

        .nav-item.active {
            background: rgba(255,255,255,0.2);
            color: white;
            font-weight: 600;
        }

        .user-profile {
            padding: 1rem;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        .main-content {
            flex: 1;
            display: flex;
            flex-direction: column;
        }

        .header {
            background: var(--bg-card);
            border-bottom: 1px solid var(--border);
            padding: 1rem 1.5rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: var(--shadow);
        }

        .header-title {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .content-area {
            flex: 1;
            overflow-y: auto;
            padding: 1.5rem;
        }

        .view-section {
            display: none;
        }

        .view-section.active {
            display: block;
        }

        .card {
            background: var(--bg-card);
            border-radius: 0.75rem;
            padding: 1.5rem;
            box-shadow: var(--shadow);
            margin-bottom: 1.5rem;
        }

        .card-title {
            font-size: 1.125rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .btn {
            padding: 0.625rem 1.25rem;
            border-radius: 0.5rem;
            border: none;
            font-weight: 500;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            transition: all 0.2s;
        }

        .btn-primary {
            background: var(--primary);
            color: white;
        }

        .btn-success {
            background: var(--success);
            color: white;
        }

        .btn-danger {
            background: var(--danger);
            color: white;
        }

        .btn-outline {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .table-container {
            background: var(--bg-card);
            border-radius: 0.75rem;
            overflow: auto;
            box-shadow: var(--shadow);
            max-height: 600px;
        }

        .table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.875rem;
        }

        .table thead {
            background: var(--bg-primary);
            position: sticky;
            top: 0;
            z-index: 10;
        }

        .table th {
            padding: 0.75rem;
            text-align: left;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.75rem;
            color: var(--text-secondary);
            border-bottom: 2px solid var(--border);
        }

        .table td {
            padding: 0.75rem;
            border-bottom: 1px solid var(--border);
        }

        .table tbody tr:hover {
            background: var(--bg-primary);
        }

        .badge {
            padding: 0.25rem 0.75rem;
            border-radius: 9999px;
            font-size: 0.75rem;
            font-weight: 600;
            display: inline-block;
        }

        .badge-blue { background: rgba(59, 130, 246, 0.1); color: #2563eb; }
        .badge-green { background: rgba(16, 185, 129, 0.1); color: #059669; }
        .badge-yellow { background: rgba(245, 158, 11, 0.1); color: #d97706; }
        .badge-red { background: rgba(239, 68, 68, 0.1); color: #dc2626; }
        .badge-purple { background: rgba(139, 92, 246, 0.1); color: #7c3aed; }

        .form-group {
            margin-bottom: 1rem;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            font-size: 0.875rem;
        }

        .form-control {
            width: 100%;
            padding: 0.625rem 1rem;
            border: 1px solid var(--border);
            border-radius: 0.5rem;
            background: var(--bg-card);
            color: var(--text-primary);
        }

        .form-control:focus {
            outline: none;
            border-color: var(--primary);
            box-shadow: 0 0 0 3px rgba(37, 99, 235, 0.1);
        }

        .modal-overlay {
            position: fixed;
            inset: 0;
            background: rgba(0, 0, 0, 0.5);
            display: none;
            align-items: center;
            justify-content: center;
            z-index: 1000;
        }

        .modal-overlay.active {
            display: flex;
        }

        .modal {
            background: var(--bg-card);
            border-radius: 1rem;
            padding: 2rem;
            max-width: 800px;
            width: 90%;
            max-height: 90vh;
            overflow-y: auto;
        }

        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }

        .modal-title {
            font-size: 1.5rem;
            font-weight: 700;
        }

        .alert {
            padding: 1rem;
            border-radius: 0.5rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: start;
            gap: 0.75rem;
        }

        .alert-warning {
            background: rgba(245, 158, 11, 0.1);
            color: #d97706;
            border: 1px solid rgba(245, 158, 11, 0.3);
        }

        .alert-danger {
            background: rgba(239, 68, 68, 0.1);
            color: #dc2626;
            border: 1px solid rgba(239, 68, 68, 0.3);
        }

        .alert-success {
            background: rgba(16, 185, 129, 0.1);
            color: #059669;
            border: 1px solid rgba(16, 185, 129, 0.3);
        }

        .alert-info {
            background: rgba(59, 130, 246, 0.1);
            color: #2563eb;
            border: 1px solid rgba(59, 130, 246, 0.3);
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: var(--bg-primary);
            border-radius: 4px;
            overflow: hidden;
            margin-top: 0.5rem;
        }

        .progress-fill {
            height: 100%;
            background: var(--primary);
            transition: width 0.3s;
        }

        .toast {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: var(--bg-card);
            padding: 1rem 1.5rem;
            border-radius: 0.5rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
            z-index: 2000;
            display: none;
            animation: slideIn 0.3s;
        }

        .toast.active {
            display: block;
        }

        @keyframes slideIn {
            from { transform: translateX(400px); }
            to { transform: translateX(0); }
        }

        .file-drop-zone {
            border: 2px dashed var(--border);
            border-radius: 0.5rem;
            padding: 2rem;
            text-align: center;
            cursor: pointer;
            transition: all 0.2s;
        }

        .file-drop-zone:hover {
            border-color: var(--primary);
            background: rgba(37, 99, 235, 0.05);
        }

        .file-drop-zone.active {
            border-color: var(--primary);
            background: rgba(37, 99, 235, 0.1);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-bottom: 1.5rem;
        }

        .stat-card {
            background: var(--bg-card);
            padding: 1.5rem;
            border-radius: 0.75rem;
            box-shadow: var(--shadow);
            border-left: 4px solid var(--primary);
        }

        .stat-value {
            font-size: 2rem;
            font-weight: 700;
        }

        .stat-label {
            font-size: 0.875rem;
            color: var(--text-secondary);
            margin-top: 0.25rem;
        }

        .loading-spinner {
            border: 3px solid rgba(0,0,0,0.1);
            border-top: 3px solid var(--primary);
            border-radius: 50%;
            width: 40px;
            height: 40px;
            animation: spin 1s linear infinite;
            margin: 2rem auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hidden { display: none !important; }
    </style>
</head>
<body>
    <div class="app-container">
        <!-- Sidebar -->
        <div class="sidebar">
            <div class="sidebar-header">
                <h1 class="sidebar-title">SICIT v5.0</h1>
                <p style="font-size: 0.875rem; opacity: 0.8;">Sistema Lukers</p>
            </div>

            <nav class="nav-menu" id="navMenu"></nav>

            <div class="user-profile">
                <div style="font-weight: 600;" id="userName">Usuario</div>
                <div style="font-size: 0.875rem; opacity: 0.8;" id="userRole">Rol</div>
            </div>
        </div>

        <!-- Main Content -->
        <div class="main-content">
            <header class="header">
                <h2 class="header-title" id="pageTitle">Dashboard</h2>
                <div style="display: flex; gap: 1rem;">
                    <button class="btn btn-outline" onclick="toggleDarkMode()" title="Cambiar tema">🌙</button>
                </div>
            </header>

            <div class="content-area">
                <!-- Dashboard -->
                <div class="view-section active" id="view-dashboard">
                    <div class="stats-grid">
                        <div class="stat-card">
                            <div class="stat-value" id="statInventario">0</div>
                            <div class="stat-label">Variantes en Inventario</div>
                        </div>
                        <div class="stat-card" style="border-left-color: var(--success);">
                            <div class="stat-value" id="statUnidades">0</div>
                            <div class="stat-label">Unidades Totales</div>
                        </div>
                        <div class="stat-card" style="border-left-color: var(--warning);">
                            <div class="stat-value" id="statBloqueadas">0</div>
                            <div class="stat-label">Unidades Bloqueadas</div>
                        </div>
                        <div class="stat-card" style="border-left-color: var(--danger);">
                            <div class="stat-value" id="statOrdenes">0</div>
                            <div class="stat-label">Órdenes Activas</div>
                        </div>
                    </div>

                    <div class="card">
                        <h3 class="card-title">Acceso Rápido</h3>
                        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem;">
                            <button class="btn btn-primary" onclick="cambiarVista('inventario')" style="padding: 1.5rem; justify-content: center;">
                                📦 Gestionar Inventario
                            </button>
                            <button class="btn btn-success" onclick="cambiarVista('ordenes')" style="padding: 1.5rem; justify-content: center;">
                                📋 Crear Orden
                            </button>
                            <button class="btn btn-outline" onclick="cambiarVista('productos-system')" style="padding: 1.5rem; justify-content: center;">
                                📊 Productos System
                            </button>
                        </div>
                    </div>

                    <div class="card">
                        <h3 class="card-title">Alertas del Sistema</h3>
                        <div id="alertasSistema"></div>
                        
                        <div style="margin-top: 1.5rem; padding-top: 1.5rem; border-top: 1px solid var(--border);">
                            <h4 style="font-size: 1rem; margin-bottom: 1rem;">Gestión de Datos</h4>
                            <div style="display: flex; gap: 0.5rem;">
                                <button class="btn btn-outline" onclick="exportarTodosDatos()">
                                    💾 Exportar Todo
                                </button>
                                <button class="btn btn-danger" onclick="limpiarTodosDatos()">
                                    🗑️ Limpiar Todos los Datos
                                </button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Gestión de Inventario (Supervisor Picking) -->
                <div class="view-section" id="view-inventario">
                    <div class="card">
                        <h3 class="card-title">Gestión de Inventario</h3>
                        
                        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1rem; margin-bottom: 1.5rem;">
                            <button class="btn btn-primary" onclick="mostrarSubidaMasiva()">
                                📤 Subir Inventario Masivo (Excel)
                            </button>
                            <button class="btn btn-success" onclick="mostrarAgregarIndividual()">
                                ➕ Agregar Producto Individual
                            </button>
                            <button class="btn btn-outline" onclick="mostrarModificarMasivo()">
                                ✏️ Modificar/Eliminar Masivo
                            </button>
                            <button class="btn btn-outline" onclick="exportarInventario()">
                                💾 Exportar Inventario
                            </button>
                        </div>

                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Buscar por variante o ubicación..." id="buscarInventario" oninput="filtrarInventario()">
                        </div>

                        <div class="table-container">
                            <table class="table">
                                <thead>
                                    <tr>
                                        <th>Variante</th>
                                        <th>Ubicación</th>
                                        <th>Stock Físico</th>
                                        <th>Stock Bloqueado</th>
                                        <th>Stock Disponible</th>
                                        <th>Acciones</th>
                                    </tr>
                                </thead>
                                <tbody id="inventarioTableBody"></tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <!-- Productos System -->
                <div class="view-section" id="view-productos-system">
                    <div class="card">
                        <h3 class="card-title">Productos System (Base de Datos)</h3>
                        
                        <div style="display: flex; gap: 1rem; margin-bottom: 1.5rem;">
                            <button class="btn btn-primary" onclick="mostrarSubirProductosSystem()">
                                📤 Subir Productos System (Excel)
                            </button>
                            <button class="btn btn-outline" onclick="verificarDiscrepancias()">
                                🔍 Verificar Discrepancias
                            </button>
                        </div>

                        <div id="discrepanciasAlert"></div>

                        <div class="table-container">
                            <table class="table">
                                <thead>
                                    <tr>
                                        <th>Variante</th>
                                        <th>Código Comercial</th>
                                        <th>Descripción</th>
                                        <th>Marca</th>
                                        <th>Talla</th>
                                        <th>PVP</th>
                                        <th>Stk Fin (Sistema)</th>
                                        <th>Stock Físico</th>
                                        <th>Estado</th>
                                    </tr>
                                </thead>
                                <tbody id="productosSystemTableBody"></tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <!-- Crear Órdenes (Producto) -->
                <div class="view-section" id="view-ordenes">
                    <div class="card">
                        <h3 class="card-title">Gestión de Órdenes</h3>
                        
                        <button class="btn btn-primary" onclick="mostrarCrearOrden()" style="margin-bottom: 1.5rem;">
                            ➕ Crear Nueva Orden (Excel)
                        </button>

                        <div class="table-container">
                            <table class="table">
                                <thead>
                                    <tr>
                                        <th>ID Orden</th>
                                        <th>Fecha Creación</th>
                                        <th>Total Unidades</th>
                                        <th>Estado</th>
                                        <th>Progreso</th>
                                        <th>Acciones</th>
                                    </tr>
                                </thead>
                                <tbody id="ordenesTableBody"></tbody>
                            </table>
                        </div>
                    </div>
                </div>

                <!-- Picking -->
                <div class="view-section" id="view-picking">
                    <div class="card">
                        <h3 class="card-title">Estación de Picking</h3>
                        
                        <div id="pickingOrdenesContainer"></div>
                    </div>
                </div>

                <!-- Packing -->
                <div class="view-section" id="view-packing">
                    <div class="card">
                        <h3 class="card-title">Estación de Packing</h3>
                        
                        <div id="packingOrdenesContainer"></div>
                    </div>
                </div>

                <!-- Reclasificación -->
                <div class="view-section" id="view-reclasificacion">
                    <div class="card">
                        <h3 class="card-title">Reclasificación de Productos</h3>
                        
                        <div class="table-container">
                            <table class="table">
                                <thead>
                                    <tr>
                                        <th>Variante Original</th>
                                        <th>Motivo</th>
                                        <th>Cantidad</th>
                                        <th>Nueva Variante</th>
                                        <th>Nueva Ubicación</th>
                                        <th>Estado</th>
                                        <th>Acciones</th>
                                    </tr>
                                </thead>
                                <tbody id="reclasificacionTableBody"></tbody>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal Subida Masiva -->
    <div class="modal-overlay" id="modalSubidaMasiva">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title">Subir Inventario Masivo</h3>
                <button onclick="cerrarModal('modalSubidaMasiva')" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            </div>
            
            <div class="alert alert-info">
                <strong>Formato requerido:</strong> Excel con columnas: <strong>Variante, Ubicación, Stock Físico</strong>
                <br>Soporta hasta 60,000 filas con procesamiento optimizado.
            </div>

            <div class="file-drop-zone" id="dropZoneMasivo" onclick="document.getElementById('fileInputMasivo').click()">
                <p style="font-size: 1.125rem; font-weight: 600; margin-bottom: 0.5rem;">📁 Arrastra tu archivo aquí</p>
                <p style="color: var(--text-secondary);">o haz clic para seleccionar</p>
                <input type="file" id="fileInputMasivo" accept=".xlsx,.xls" style="display: none;" onchange="procesarInventarioMasivo(event)">
            </div>

            <div id="progressMasivo" class="hidden" style="margin-top: 1rem;">
                <p>Procesando: <span id="progressText">0</span>%</p>
                <div class="progress-bar">
                    <div class="progress-fill" id="progressFill" style="width: 0%"></div>
                </div>
            </div>
        </div>
    </div>

    <!-- Modal Agregar Individual -->
    <div class="modal-overlay" id="modalAgregarIndividual">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title">Agregar Producto Individual</h3>
                <button onclick="cerrarModal('modalAgregarIndividual')" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            </div>
            
            <form onsubmit="guardarProductoIndividual(event)">
                <div class="form-group">
                    <label class="form-label">Variante *</label>
                    <input type="text" class="form-control" id="varianteIndividual" required>
                </div>
                <div class="form-group">
                    <label class="form-label">Ubicación * (Ej: A001-01-01)</label>
                    <input type="text" class="form-control" id="ubicacionIndividual" required>
                </div>
                <div class="form-group">
                    <label class="form-label">Stock Físico *</label>
                    <input type="number" class="form-control" id="stockIndividual" min="1" required>
                </div>
                <div style="display: flex; gap: 1rem; justify-content: flex-end; margin-top: 1.5rem;">
                    <button type="button" class="btn btn-outline" onclick="cerrarModal('modalAgregarIndividual')">Cancelar</button>
                    <button type="submit" class="btn btn-primary">Guardar</button>
                </div>
            </form>
        </div>
    </div>

    <!-- Modal Crear Orden -->
    <div class="modal-overlay" id="modalCrearOrden">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title">Crear Nueva Orden</h3>
                <button onclick="cerrarModal('modalCrearOrden')" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            </div>
            
            <div class="alert alert-info">
                <strong>Formato requerido:</strong> Excel con columnas:<br>
                <strong>Variante, LUKERS EL SOL, LUKERS TRU PIZARRO, LUKERS LA MARINA, LUKERS PROLONGACIÓN IQUITOS, LUKERS CHI P. RUIZ, LUKERS TARAPOTO, LUKERS MENDIOLA, LUKERS ALFONSO UGARTE, LUKERS IQT LORES, LUKERS JIRON</strong>
            </div>

            <div class="file-drop-zone" onclick="document.getElementById('fileInputOrden').click()">
                <p style="font-size: 1.125rem; font-weight: 600; margin-bottom: 0.5rem;">📁 Subir Orden (Excel)</p>
                <input type="file" id="fileInputOrden" accept=".xlsx,.xls" style="display: none;" onchange="procesarOrden(event)">
            </div>
        </div>
    </div>

    <!-- Modal Productos System -->
    <div class="modal-overlay" id="modalProductosSystem">
        <div class="modal">
            <div class="modal-header">
                <h3 class="modal-title">Subir Productos System</h3>
                <button onclick="cerrarModal('modalProductosSystem')" style="background: none; border: none; font-size: 1.5rem; cursor: pointer;">×</button>
            </div>
            
            <div class="alert alert-info">
                <strong>Columnas requeridas:</strong> VARIANTE, CODIGO COMERCIAL, DESCRIPCIÓN, Kardex, PVP, Stk Fin, Genero, Mundo, Linea, MARCA, COLOR, TALLA, TEMPORADA_MUNDO
            </div>

            <div class="file-drop-zone" onclick="document.getElementById('fileInputProductosSystem').click()">
                <p style="font-size: 1.125rem; font-weight: 600; margin-bottom: 0.5rem;">📁 Subir Archivo</p>
                <input type="file" id="fileInputProductosSystem" accept=".xlsx,.xls" style="display: none;" onchange="procesarProductosSystem(event)">
            </div>
        </div>
    </div>

    <!-- Toast -->
    <div class="toast" id="toast"></div>

    <!-- Loading Overlay para carga masiva -->
    <div class="modal-overlay" id="loadingOverlay" style="z-index: 9999;">
        <div style="background: var(--bg-card); padding: 3rem; border-radius: 1rem; text-align: center; min-width: 400px;">
            <div class="loading-spinner" style="margin: 0 auto 1.5rem;"></div>
            <h3 style="font-size: 1.5rem; font-weight: 700; margin-bottom: 0.5rem;">Procesando datos...</h3>
            <p style="color: var(--text-secondary); margin-bottom: 1rem;">Por favor no cierres esta ventana</p>
            <div class="progress-bar" style="width: 100%;">
                <div class="progress-fill" id="loadingProgress" style="width: 0%"></div>
            </div>
            <p style="margin-top: 0.5rem; font-size: 0.875rem; color: var(--text-secondary);">
                <span id="loadingText">Cargando archivo...</span>
            </p>
        </div>
    </div>

    <script>
// ==========================================
// CONFIGURACIÓN DE GOOGLE SHEETS API
// ==========================================

// ⚠️ REEMPLAZA ESTOS VALORES CON LOS TUYOS
const GOOGLE_CONFIG = {
    CLIENT_ID: '309993250500-otauf9c2kjib3bmf8btu9baqmmkm4sur.apps.googleusercontent.com', // Reemplaza con tu Client ID de Google Cloud
    API_KEY: '', // Opcional, puedes dejarlo vacío
    SPREADSHEET_ID: '1_OoyX3z5Itpe5VTx-zFbYnNqM-WNeqVuiB6QszHuTWU', // Reemplaza con el ID de tu Google Sheet
    SCOPES: 'https://www.googleapis.com/auth/spreadsheets'
};

let gapiInited = false;
let gisInited = false;
let tokenClient;
let accessToken = null;

        // Firebase Config
        const firebaseConfig = {
            apiKey: "AIzaSyDHuWQuY-HIZTf30JfXL_WCEwLaf1XkZ8E",
            authDomain: "lukers-cd.firebaseapp.com",
            projectId: "lukers-cd",
            storageBucket: "lukers-cd.firebasestorage.app",
            messagingSenderId: "386476443838",
            appId: "1:386476443838:web:fa8e19559dd61ec1fbb6ef"
        };

        firebase.initializeApp(firebaseConfig);
        const db = firebase.firestore();

        // Variables Globales
        let currentUser = { nombre: 'Usuario', rol: 'supervisor_picking' };
        let inventario = [];
        let productosSystem = [];
        let ordenes = [];
        let itemsReclasificacion = [];
        let darkMode = false;
        let datosEnMemoria = false;
        let cargaMasivaEnProceso = false; // Flag para evitar guardado durante carga masiva

        // SISTEMA DE PERSISTENCIA CON FIREBASE
        async function guardarInventarioFirebase() {
            try {
                const batch = db.batch();
                
                // Limpiar colección primero
                const snapshot = await db.collection('inventario').get();
                snapshot.docs.forEach(doc => {
                    batch.delete(doc.ref);
                });
                
                // Guardar nuevo inventario
                inventario.forEach(item => {
                    const docRef = db.collection('inventario').doc(`${item.variante}_${item.ubicacion}`);
                    batch.set(docRef, item);
                });
                
                await batch.commit();
                console.log('Inventario guardado en Firebase');
                return true;
            } catch (error) {
                console.error('Error al guardar inventario:', error);
                mostrarToast('Error al guardar en Firebase. Datos guardados localmente.', 'warning');
                guardarDatosLocal();
                return false;
            }
        }

        async function cargarInventarioFirebase() {
            try {
                const snapshot = await db.collection('inventario').get();
                inventario = [];
                snapshot.forEach(doc => {
                    inventario.push(doc.data());
                });
                console.log(`${inventario.length} items de inventario cargados desde Firebase`);
                return true;
            } catch (error) {
                console.error('Error al cargar inventario:', error);
                return false;
            }
        }

        async function guardarProductosSystemFirebase() {
            try {
                const batch = db.batch();
                
                const snapshot = await db.collection('productosSystem').get();
                snapshot.docs.forEach(doc => {
                    batch.delete(doc.ref);
                });
                
                productosSystem.forEach(prod => {
                    const docRef = db.collection('productosSystem').doc(prod.variante);
                    batch.set(docRef, prod);
                });
                
                await batch.commit();
                console.log('Productos System guardados en Firebase');
                return true;
            } catch (error) {
                console.error('Error al guardar productos system:', error);
                return false;
            }
        }

        async function cargarProductosSystemFirebase() {
            try {
                const snapshot = await db.collection('productosSystem').get();
                productosSystem = [];
                snapshot.forEach(doc => {
                    productosSystem.push(doc.data());
                });
                console.log(`${productosSystem.length} productos system cargados desde Firebase`);
                return true;
            } catch (error) {
                console.error('Error al cargar productos system:', error);
                return false;
            }
        }

        async function guardarOrdenesFirebase() {
            try {
                const batch = db.batch();
                
                const snapshot = await db.collection('ordenes').get();
                snapshot.docs.forEach(doc => {
                    batch.delete(doc.ref);
                });
                
                ordenes.forEach(orden => {
                    const docRef = db.collection('ordenes').doc(orden.id);
                    batch.set(docRef, {
                        ...orden,
                        fecha: orden.fecha.toISOString(),
                        fechaCierre: orden.fechaCierre ? orden.fechaCierre.toISOString() : null
                    });
                });
                
                await batch.commit();
                console.log('Órdenes guardadas en Firebase');
                return true;
            } catch (error) {
                console.error('Error al guardar órdenes:', error);
                return false;
            }
        }

        async function cargarOrdenesFirebase() {
            try {
                const snapshot = await db.collection('ordenes').get();
                ordenes = [];
                snapshot.forEach(doc => {
                    const data = doc.data();
                    ordenes.push({
                        ...data,
                        fecha: new Date(data.fecha),
                        fechaCierre: data.fechaCierre ? new Date(data.fechaCierre) : null
                    });
                });
                console.log(`${ordenes.length} órdenes cargadas desde Firebase`);
                return true;
            } catch (error) {
                console.error('Error al cargar órdenes:', error);
                return false;
            }
        }

        async function guardarReclasificacionFirebase() {
            try {
                const batch = db.batch();
                
                const snapshot = await db.collection('reclasificacion').get();
                snapshot.docs.forEach(doc => {
                    batch.delete(doc.ref);
                });
                
                itemsReclasificacion.forEach(item => {
                    const docRef = db.collection('reclasificacion').doc(item.id);
                    batch.set(docRef, item);
                });
                
                await batch.commit();
                console.log('Reclasificación guardada en Firebase');
                return true;
            } catch (error) {
                console.error('Error al guardar reclasificación:', error);
                return false;
            }
        }

        async function cargarReclasificacionFirebase() {
            try {
                const snapshot = await db.collection('reclasificacion').get();
                itemsReclasificacion = [];
                snapshot.forEach(doc => {
                    itemsReclasificacion.push(doc.data());
                });
                console.log(`${itemsReclasificacion.length} items de reclasificación cargados desde Firebase`);
                return true;
            } catch (error) {
                console.error('Error al cargar reclasificación:', error);
                return false;
            }
        }

        // Función principal para guardar todo (con control de carga masiva)
        async function guardarDatos() {
            // Si estamos en carga masiva, no guardar todavía
            if (cargaMasivaEnProceso) {
                console.log('Carga masiva en proceso, guardado pospuesto');
                return;
            }
            
            try {
                await Promise.all([
                    guardarInventarioFirebase(),
                    guardarProductosSystemFirebase(),
                    guardarOrdenesFirebase(),
                    guardarReclasificacionFirebase()
                ]);
                datosEnMemoria = false;
            } catch (error) {
                console.error('Error al guardar datos:', error);
                guardarDatosLocal(); // Fallback a localStorage
            }
        }

        // Función principal para cargar todo
        async function cargarDatos() {
            try {
                mostrarToast('Cargando datos desde Firebase...', 'info');
                
                await Promise.all([
                    cargarInventarioFirebase(),
                    cargarProductosSystemFirebase(),
                    cargarOrdenesFirebase(),
                    cargarReclasificacionFirebase()
                ]);
                
                datosEnMemoria = true;
                return true;
            } catch (error) {
                console.error('Error al cargar datos:', error);
                cargarDatosLocal(); // Fallback a localStorage
                return false;
            }
        }

        // Fallback a localStorage
        function guardarDatosLocal() {
            try {
                localStorage.setItem('sicit_inventario', JSON.stringify(inventario));
                localStorage.setItem('sicit_productosSystem', JSON.stringify(productosSystem));
                localStorage.setItem('sicit_ordenes', JSON.stringify(ordenes));
                localStorage.setItem('sicit_reclasificacion', JSON.stringify(itemsReclasificacion));
                console.log('Datos guardados en localStorage (fallback)');
            } catch (error) {
                console.error('Error al guardar datos localmente:', error);
            }
        }

        function cargarDatosLocal() {
            try {
                const invGuardado = localStorage.getItem('sicit_inventario');
                const prodGuardado = localStorage.getItem('sicit_productosSystem');
                const ordGuardado = localStorage.getItem('sicit_ordenes');
                const reclaGuardado = localStorage.getItem('sicit_reclasificacion');

                if (invGuardado) inventario = JSON.parse(invGuardado);
                if (prodGuardado) productosSystem = JSON.parse(prodGuardado);
                if (ordGuardado) {
                    ordenes = JSON.parse(ordGuardado);
                    ordenes.forEach(orden => {
                        if (orden.fecha) orden.fecha = new Date(orden.fecha);
                        if (orden.fechaCierre) orden.fechaCierre = new Date(orden.fechaCierre);
                    });
                }
                if (reclaGuardado) itemsReclasificacion = JSON.parse(reclaGuardado);

                console.log('Datos cargados desde localStorage');
            } catch (error) {
                console.error('Error al cargar datos localmente:', error);
            }
        }

        const TIENDAS_LUKERS = [
            'LUKERS EL SOL',
            'LUKERS TRU PIZARRO',
            'LUKERS LA MARINA',
            'LUKERS PROLONGACIÓN IQUITOS',
            'LUKERS CHI P. RUIZ',
            'LUKERS TARAPOTO',
            'LUKERS MENDIOLA',
            'LUKERS ALFONSO UGARTE',
            'LUKERS IQT LORES',
            'LUKERS JIRON'
        ];

        // Utilidades
        function mostrarToast(mensaje, tipo = 'info') {
            const toast = document.getElementById('toast');
            toast.textContent = mensaje;
            toast.className = `toast active alert-${tipo}`;
            setTimeout(() => toast.classList.remove('active'), 3000);
        }

        function cerrarModal(id) {
            document.getElementById(id).classList.remove('active');
        }

        function mostrarModal(id) {
            document.getElementById(id).classList.add('active');
        }

        function cambiarVista(vista) {
            document.querySelectorAll('.view-section').forEach(v => v.classList.remove('active'));
            document.getElementById(`view-${vista}`).classList.add('active');
            document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
            document.querySelector(`[data-view="${vista}"]`)?.classList.add('active');
            document.getElementById('pageTitle').textContent = vista.charAt(0).toUpperCase() + vista.slice(1).replace(/-/g, ' ');
        }

        function toggleDarkMode() {
            darkMode = !darkMode;
            document.documentElement.setAttribute('data-theme', darkMode ? 'dark' : 'light');
        }

        // Inicialización
        async function init() {
            generarMenu();
            
            // Intentar cargar desde Firebase
            const cargaExitosa = await cargarDatos();
            
            // Si no hay datos en Firebase, cargar datos iniciales de ejemplo
            if (inventario.length === 0 && productosSystem.length === 0) {
                cargarDatosIniciales();
                // Guardar datos iniciales en Firebase
                await guardarDatos();
            }
            
            actualizarDashboard();
            renderizarInventario();
            renderizarProductosSystem();
            renderizarOrdenes();
            renderizarPicking();
            renderizarPacking();
            renderizarReclasificacion();
            
            if (cargaExitosa) {
                mostrarToast('Datos sincronizados desde Firebase ✓', 'success');
            } else {
                mostrarToast('Usando datos locales. Verifica conexión a Firebase.', 'warning');
            }
        }

        function generarMenu() {
            const menus = [
                { id: 'dashboard', icon: '🏠', label: 'Dashboard' },
                { id: 'inventario', icon: '📦', label: 'Inventario' },
                { id: 'productos-system', icon: '📊', label: 'Productos System' },
                { id: 'ordenes', icon: '📋', label: 'Órdenes' },
                { id: 'picking', icon: '🔍', label: 'Picking' },
                { id: 'packing', icon: '📦', label: 'Packing' },
                { id: 'reclasificacion', icon: '♻️', label: 'Reclasificación' }
            ];

            document.getElementById('navMenu').innerHTML = menus.map(m => `
                <div class="nav-item ${m.id === 'dashboard' ? 'active' : ''}" data-view="${m.id}" onclick="cambiarVista('${m.id}')">
                    <span>${m.icon}</span>
                    <span>${m.label}</span>
                </div>
            `).join('');
        }

        function cargarDatosIniciales() {
            // Datos de ejemplo
            inventario = [
                { variante: '1234567890123', ubicacion: 'A001-01-01', stockFisico: 50, stockBloqueado: 0 },
                { variante: '1234567890124', ubicacion: 'A001-01-02', stockFisico: 30, stockBloqueado: 0 },
                { variante: '1234567890123', ubicacion: 'B002-02-01', stockFisico: 20, stockBloqueado: 0 }
            ];

            productosSystem = [
                { 
                    variante: '1234567890123', 
                    codigoComercial: 'ABC123', 
                    descripcion: 'Producto de prueba',
                    marca: 'NIKE',
                    talla: 'M',
                    pvp: 89.90,
                    stkFin: 70,
                    genero: 'Unisex',
                    mundo: 'Deportivo',
                    linea: 'Casual',
                    color: 'Negro',
                    temporada: '2024-A'
                }
            ];

            ordenes = [];
        }

        function actualizarDashboard() {
            const totalUnidades = inventario.reduce((sum, item) => sum + item.stockFisico, 0);
            const totalBloqueadas = inventario.reduce((sum, item) => sum + item.stockBloqueado, 0);
            
            document.getElementById('statInventario').textContent = new Set(inventario.map(i => i.variante)).size;
            document.getElementById('statUnidades').textContent = totalUnidades;
            document.getElementById('statBloqueadas').textContent = totalBloqueadas;
            document.getElementById('statOrdenes').textContent = ordenes.filter(o => o.estado !== 'Completada').length;
        }

        function renderizarInventario() {
            const busqueda = document.getElementById('buscarInventario')?.value.toLowerCase() || '';
            const filtrado = inventario.filter(item => 
                item.variante.toLowerCase().includes(busqueda) ||
                item.ubicacion.toLowerCase().includes(busqueda)
            );

            document.getElementById('inventarioTableBody').innerHTML = filtrado.map(item => `
                <tr>
                    <td><strong>${item.variante}</strong></td>
                    <td>${item.ubicacion}</td>
                    <td>${item.stockFisico}</td>
                    <td style="color: var(--warning);">${item.stockBloqueado}</td>
                    <td style="color: var(--success);"><strong>${item.stockFisico - item.stockBloqueado}</strong></td>
                    <td>
                        <button class="btn btn-outline" style="padding: 0.25rem 0.75rem; font-size: 0.875rem;" onclick="editarInventario('${item.variante}', '${item.ubicacion}')">Editar</button>
                        <button class="btn btn-danger" style="padding: 0.25rem 0.75rem; font-size: 0.875rem; margin-left: 0.5rem;" onclick="eliminarInventario('${item.variante}', '${item.ubicacion}')">Eliminar</button>
                    </td>
                </tr>
            `).join('');
        }

        function filtrarInventario() {
            renderizarInventario();
        }

        // Funciones de Modal
        function mostrarSubidaMasiva() {
            mostrarModal('modalSubidaMasiva');
        }

        function mostrarAgregarIndividual() {
            document.getElementById('varianteIndividual').value = '';
            document.getElementById('ubicacionIndividual').value = '';
            document.getElementById('stockIndividual').value = '';
            mostrarModal('modalAgregarIndividual');
        }

        function mostrarModificarMasivo() {
            mostrarToast('Función de modificación masiva disponible. Sube un Excel con: Variante, Ubicación, Acción (MODIFICAR/ELIMINAR), Stock Físico', 'info');
        }

        function mostrarCrearOrden() {
            mostrarModal('modalCrearOrden');
        }

        function mostrarSubirProductosSystem() {
            mostrarModal('modalProductosSystem');
        }

        // Procesamiento de Inventario Masivo (OPTIMIZADO PARA 60K FILAS)
        async function procesarInventarioMasivo(event) {
            const file = event.target.files[0];
            if (!file) return;

            // ACTIVAR FLAG DE CARGA MASIVA
            cargaMasivaEnProceso = true;
            
            // Mostrar overlay de loading
            document.getElementById('loadingOverlay').classList.add('active');
            document.getElementById('loadingText').textContent = 'Procesando inventario...';
            cerrarModal('modalSubidaMasiva');
            
            const reader = new FileReader();
            reader.onload = async function(e) {
                try {
                    const data = new Uint8Array(e.target.result);
                    const workbook = XLSX.read(data, { type: 'array' });
                    const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
                    const jsonData = XLSX.utils.sheet_to_json(firstSheet);

                    const totalRows = jsonData.length;
                    let procesados = 0;
                    const BATCH_SIZE = 5000;

                    // PROCESAR TODO EN MEMORIA PRIMERO
                    document.getElementById('loadingText').textContent = `Procesando ${totalRows} filas...`;
                    
                    for (let i = 0; i < jsonData.length; i += BATCH_SIZE) {
                        const batch = jsonData.slice(i, i + BATCH_SIZE);
                        
                        batch.forEach(row => {
                            const variante = String(row.Variante || row.variante || '').trim();
                            const ubicacion = String(row.Ubicacion || row.ubicacion || row['Ubicación'] || '').trim().toUpperCase();
                            const stockFisico = parseInt(row['Stock Físico'] || row['Stock Fisico'] || row.Stock || 0);

                            if (!variante || !ubicacion || !stockFisico) return;

                            const existente = inventario.find(item => 
                                item.variante === variante && item.ubicacion === ubicacion
                            );

                            if (existente) {
                                existente.stockFisico += stockFisico;
                            } else {
                                inventario.push({
                                    variante,
                                    ubicacion,
                                    stockFisico,
                                    stockBloqueado: 0
                                });
                            }
                        });

                        procesados += batch.length;
                        const progreso = Math.round((procesados / totalRows) * 90); // 90% para procesamiento
                        document.getElementById('loadingProgress').style.width = progreso + '%';
                        document.getElementById('loadingText').textContent = `Procesando: ${procesados} de ${totalRows} filas`;

                        await new Promise(resolve => setTimeout(resolve, 0));
                    }

                    // GUARDAR EN GOOGLE SHEETS
                    document.getElementById('loadingText').textContent = 'Guardando en Google Sheets...';
                    document.getElementById('loadingProgress').style.width = '95%';
                    
                    await guardarInventarioSheetsOptimizado(inventario);
                    
                    document.getElementById('loadingProgress').style.width = '100%';
                    
                    // DESACTIVAR FLAG
                    cargaMasivaEnProceso = false;

                    mostrarToast(`✓ ${totalRows} filas procesadas y guardadas`, 'success');
                    document.getElementById('loadingOverlay').classList.remove('active');
                    
                    renderizarInventario();
                    actualizarDashboard();
                    
                } catch (error) {
                    cargaMasivaEnProceso = false;
                    document.getElementById('loadingOverlay').classList.remove('active');
                    console.error(error);
                    mostrarToast('Error al procesar archivo', 'danger');
                }
            };
            reader.readAsArrayBuffer(file);
        }

        // Guardar inventario en Sheets de forma OPTIMIZADA
        async function guardarInventarioSheetsOptimizado(inventarioCompleto) {
            try {
                document.getElementById('loadingText').textContent = 'Guardando en Google Sheets...';
                
                const valores = [
                    ['variante', 'ubicacion', 'stockFisico', 'stockBloqueado'], // Headers
                    ...inventarioCompleto.map(item => [
                        item.variante,
                        item.ubicacion,
                        item.stockFisico,
                        item.stockBloqueado
                    ])
                ];

                await escribirHoja('inventario', valores);
                console.log(`${inventarioCompleto.length} items guardados en Sheets`);
                return true;
            } catch (error) {
                console.error('Error al guardar inventario optimizado:', error);
                throw error;
            }
        }

        async function guardarEnFirebase() {
            // Firebase deshabilitado por errores de permisos
            // Usar localStorage en su lugar
            guardarDatos();
        }

        async function limpiarTodosDatos() {
            if (confirm('⚠️ ADVERTENCIA: Esto eliminará TODOS los datos en Google Sheets para TODOS los usuarios.\n\n¿Estás seguro de continuar?')) {
                if (confirm('Esta acción NO se puede deshacer y afectará a TODO el equipo. ¿Confirmas?')) {
                    try {
                        document.getElementById('loadingOverlay').classList.add('active');
                        document.getElementById('loadingText').textContent = 'Limpiando Google Sheets...';
                        
                        // Limpiar todas las hojas
                        await Promise.all([
                            escribirHoja('inventario', [['variante', 'ubicacion', 'stockFisico', 'stockBloqueado']]),
                            escribirHoja('productosSystem', [['variante', 'codigoComercial', 'descripcion', 'pvp', 'stkFin', 'marca', 'talla', 'genero', 'color', 'temporada']]),
                            escribirHoja('ordenes', [['id', 'fecha', 'estado', 'totalUnidades', 'items', 'hojaRutaPicking', 'hojaPacking', 'cantidadesEncontradas', 'unidadesEncontradas', 'unidadesFaltantes', 'distribucionAjustada', 'observaciones', 'prendasRechazadas', 'fechaCierre']]),
                            escribirHoja('reclasificacion', [['id', 'ordenId', 'varianteOriginal', 'cantidad', 'motivo', 'estado', 'ubicacionDestino', 'nuevaVariante']])
                        ]);
                        
                        document.getElementById('loadingOverlay').classList.remove('active');
                        console.log('Google Sheets limpiado');
                    } catch (error) {
                        console.error('Error al limpiar Google Sheets:', error);
                        document.getElementById('loadingOverlay').classList.remove('active');
                    }
                    
                    // Limpiar variables locales
                    inventario = [];
                    productosSystem = [];
                    ordenes = [];
                    itemsReclasificacion = [];
                    
                    // Re-renderizar todo
                    actualizarDashboard();
                    renderizarInventario();
                    renderizarProductosSystem();
                    renderizarOrdenes();
                    renderizarPicking();
                    renderizarPacking();
                    renderizarReclasificacion();
                    
                    mostrarToast('Todos los datos han sido eliminados de Google Sheets', 'success');
                }
            }
        }

        function exportarTodosDatos() {
            const wb = XLSX.utils.book_new();
            
            // Hoja 1: Inventario
            const wsInv = XLSX.utils.json_to_sheet(inventario);
            XLSX.utils.book_append_sheet(wb, wsInv, 'Inventario');
            
            // Hoja 2: Productos System
            const wsProd = XLSX.utils.json_to_sheet(productosSystem);
            XLSX.utils.book_append_sheet(wb, wsProd, 'Productos System');
            
            // Hoja 3: Órdenes
            const wsOrd = XLSX.utils.json_to_sheet(ordenes);
            XLSX.utils.book_append_sheet(wb, wsOrd, 'Ordenes');
            
            XLSX.writeFile(wb, `SICIT-Backup-${new Date().toISOString().split('T')[0]}.xlsx`);
            mostrarToast('Backup completo exportado', 'success');
        }

        function guardarProductoIndividual(event) {
            event.preventDefault();
            
            const variante = document.getElementById('varianteIndividual').value.trim();
            const ubicacion = document.getElementById('ubicacionIndividual').value.trim().toUpperCase();
            const stockFisico = parseInt(document.getElementById('stockIndividual').value);

            // Verificar si existe
            const existente = inventario.find(item => 
                item.variante === variante && item.ubicacion === ubicacion
            );

            if (existente) {
                if (confirm(`La variante ${variante} ya existe en ${ubicacion} con ${existente.stockFisico} unidades.\n\n¿Deseas AUMENTAR la cantidad en ${stockFisico} unidades?`)) {
                    existente.stockFisico += stockFisico;
                    mostrarToast('Stock aumentado correctamente', 'success');
                } else {
                    mostrarToast('Operación cancelada. Cambia la ubicación.', 'warning');
                    return;
                }
            } else {
                inventario.push({ variante, ubicacion, stockFisico, stockBloqueado: 0 });
                mostrarToast('Producto agregado correctamente', 'success');
            }

            cerrarModal('modalAgregarIndividual');
            renderizarInventario();
            actualizarDashboard();
            guardarDatos(); // ✅ GUARDAR CAMBIOS
        }

        function editarInventario(variante, ubicacion) {
            const item = inventario.find(i => i.variante === variante && i.ubicacion === ubicacion);
            const nuevoStock = prompt(`Editar stock para ${variante} en ${ubicacion}\nStock actual: ${item.stockFisico}`, item.stockFisico);
            
            if (nuevoStock !== null) {
                item.stockFisico = parseInt(nuevoStock);
                mostrarToast('Stock actualizado', 'success');
                renderizarInventario();
                actualizarDashboard();
                guardarDatos(); // ✅ GUARDAR CAMBIOS
            }
        }

        function eliminarInventario(variante, ubicacion) {
            if (confirm(`¿Eliminar ${variante} de ${ubicacion}?`)) {
                inventario = inventario.filter(i => !(i.variante === variante && i.ubicacion === ubicacion));
                mostrarToast('Producto eliminado', 'success');
                renderizarInventario();
                actualizarDashboard();
                guardarDatos(); // ✅ GUARDAR CAMBIOS
            }
        }

        function exportarInventario() {
            const ws = XLSX.utils.json_to_sheet(inventario);
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, 'Inventario');
            XLSX.writeFile(wb, `inventario-${Date.now()}.xlsx`);
            mostrarToast('Inventario exportado', 'success');
        }

        // Productos System (OPTIMIZADO)
        function procesarProductosSystem(event) {
            const file = event.target.files[0];
            if (!file) return;

            // ACTIVAR FLAG DE CARGA MASIVA
            cargaMasivaEnProceso = true;
            
            // Mostrar overlay de loading
            document.getElementById('loadingOverlay').classList.add('active');
            document.getElementById('loadingText').textContent = 'Procesando Productos System...';
            document.getElementById('loadingProgress').style.width = '30%';
            cerrarModal('modalProductosSystem');

            const reader = new FileReader();
            reader.onload = async function(e) {
                try {
                    const data = new Uint8Array(e.target.result);
                    const workbook = XLSX.read(data, { type: 'array' });
                    const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
                    const jsonData = XLSX.utils.sheet_to_json(firstSheet);

                    document.getElementById('loadingProgress').style.width = '60%';
                    document.getElementById('loadingText').textContent = `Procesando ${jsonData.length} productos...`;

                    productosSystem = jsonData.map(row => ({
                        variante: String(row.VARIANTE || row.variante),
                        codigoComercial: row['CODIGO COMERCIAL'] || row['Codigo Comercial'] || '',
                        descripcion: row['DESCRIPCIÓN'] || row.descripcion || '',
                        pvp: parseFloat(row.PVP || 0),
                        stkFin: parseInt(row['Stk Fin'] || row.stkFin || 0),
                        marca: row.MARCA || row.marca || '',
                        talla: row.TALLA || row.talla || '',
                        genero: row.Genero || row.genero || '',
                        color: row.COLOR || row.color || '',
                        temporada: row.TEMPORADA_MUNDO || row.temporada || ''
                    }));

                    document.getElementById('loadingProgress').style.width = '80%';
                    document.getElementById('loadingText').textContent = 'Guardando en Google Sheets...';
                    
                    // Guardar en Sheets
                    await guardarProductosSystemSheetsOptimizado();
                    
                    document.getElementById('loadingProgress').style.width = '100%';
                    
                    // DESACTIVAR FLAG
                    cargaMasivaEnProceso = false;

                    mostrarToast(`✓ ${productosSystem.length} productos cargados`, 'success');
                    document.getElementById('loadingOverlay').classList.remove('active');
                    
                    renderizarProductosSystem();
                    verificarDiscrepancias();
                    
                } catch (error) {
                    cargaMasivaEnProceso = false;
                    document.getElementById('loadingOverlay').classList.remove('active');
                    console.error(error);
                    mostrarToast('Error al procesar archivo', 'danger');
                }
            };
            reader.readAsArrayBuffer(file);
        }

        async function guardarProductosSystemSheetsOptimizado() {
            try {
                const valores = [
                    ['variante', 'codigoComercial', 'descripcion', 'pvp', 'stkFin', 'marca', 'talla', 'genero', 'color', 'temporada'],
                    ...productosSystem.map(p => [
                        p.variante, p.codigoComercial, p.descripcion, p.pvp, p.stkFin,
                        p.marca, p.talla, p.genero, p.color, p.temporada
                    ])
                ];

                await escribirHoja('productosSystem', valores);
                console.log('Productos System guardados en Sheets');
                return true;
            } catch (error) {
                console.error('Error al guardar productos system:', error);
                throw error;
            }
        }

        function renderizarProductosSystem() {
            document.getElementById('productosSystemTableBody').innerHTML = productosSystem.map(prod => {
                const stockFisico = inventario
                    .filter(i => i.variante === prod.variante)
                    .reduce((sum, i) => sum + i.stockFisico, 0);
                
                const diferencia = Math.abs(stockFisico - prod.stkFin);
                const estado = diferencia === 0 ? 'OK' : diferencia <= 5 ? 'REVISAR' : 'ALERTA';
                const colorEstado = estado === 'OK' ? 'green' : estado === 'REVISAR' ? 'yellow' : 'red';

                return `
                    <tr>
                        <td><strong>${prod.variante}</strong></td>
                        <td>${prod.codigoComercial}</td>
                        <td>${prod.descripcion}</td>
                        <td>${prod.marca}</td>
                        <td>${prod.talla}</td>
                        <td>S/ ${prod.pvp.toFixed(2)}</td>
                        <td>${prod.stkFin}</td>
                        <td>${stockFisico}</td>
                        <td><span class="badge badge-${colorEstado}">${estado}</span></td>
                    </tr>
                `;
            }).join('');
        }

        function verificarDiscrepancias() {
            const discrepancias = productosSystem.filter(prod => {
                const stockFisico = inventario
                    .filter(i => i.variante === prod.variante)
                    .reduce((sum, i) => sum + i.stockFisico, 0);
                return Math.abs(stockFisico - prod.stkFin) > 5;
            });

            const alertDiv = document.getElementById('discrepanciasAlert');
            if (discrepancias.length > 0) {
                alertDiv.innerHTML = `
                    <div class="alert alert-danger">
                        <strong>⚠️ ${discrepancias.length} variantes con discrepancias mayores a 5 unidades</strong>
                        <br>Se requiere verificación del área de picking.
                    </div>
                `;
            } else {
                alertDiv.innerHTML = '<div class="alert alert-success">✓ Todos los stocks coinciden</div>';
            }
        }

        // Procesamiento de Órdenes
        function procesarOrden(event) {
            const file = event.target.files[0];
            if (!file) return;

            mostrarToast('Procesando orden...', 'info');

            const reader = new FileReader();
            reader.onload = function(e) {
                try {
                    const data = new Uint8Array(e.target.result);
                    const workbook = XLSX.read(data, { type: 'array' });
                    const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
                    const jsonData = XLSX.utils.sheet_to_json(firstSheet);

                    // Crear orden
                    const orden = {
                        id: `ORD-${Date.now()}`,
                        fecha: new Date(),
                        estado: 'Creada',
                        items: [],
                        totalUnidades: 0
                    };

                    // Procesar cada variante
                    jsonData.forEach(row => {
                        const variante = String(row.Variante || row.variante);
                        const distribucion = {};
                        let totalVariante = 0;

                        TIENDAS_LUKERS.forEach(tienda => {
                            const cantidad = parseInt(row[tienda] || 0);
                            distribucion[tienda] = cantidad;
                            totalVariante += cantidad;
                        });

                        if (totalVariante > 0) {
                            // Buscar en inventario (ubicaciones con MENOR cantidad primero)
                            const ubicacionesDisponibles = inventario
                                .filter(inv => inv.variante === variante && (inv.stockFisico - inv.stockBloqueado) > 0)
                                .sort((a, b) => (a.stockFisico - a.stockBloqueado) - (b.stockFisico - b.stockBloqueado));

                            const asignaciones = [];
                            let pendiente = totalVariante;

                            for (const ubicacion of ubicacionesDisponibles) {
                                if (pendiente <= 0) break;
                                
                                const disponible = ubicacion.stockFisico - ubicacion.stockBloqueado;
                                const tomar = Math.min(disponible, pendiente);
                                
                                asignaciones.push({
                                    ubicacion: ubicacion.ubicacion,
                                    cantidad: tomar
                                });
                                
                                pendiente -= tomar;
                            }

                            orden.items.push({
                                variante,
                                distribucion,
                                asignaciones,
                                totalSolicitado: totalVariante,
                                totalDisponible: totalVariante - pendiente
                            });

                            orden.totalUnidades += totalVariante;
                        }
                    });

                    ordenes.push(orden);
                    
                    // Generar hoja de ruta para Picking
                    generarHojaRutaPicking(orden);
                    
                    mostrarToast('Orden creada exitosamente', 'success');
                    cerrarModal('modalCrearOrden');
                    renderizarOrdenes();
                    actualizarDashboard();
                    
                } catch (error) {
                    console.error(error);
                    mostrarToast('Error al procesar orden', 'danger');
                }
            };
            reader.readAsArrayBuffer(file);
        }

        function generarHojaRutaPicking(orden) {
            const hojaRuta = [];

            orden.items.forEach(item => {
                const prodInfo = productosSystem.find(p => p.variante === item.variante) || {};
                
                item.asignaciones.forEach(asig => {
                    hojaRuta.push({
                        'Ubicación': asig.ubicacion,
                        'Marca': prodInfo.marca || '',
                        'Código Comercial': prodInfo.codigoComercial || '',
                        'Variante': item.variante,
                        'Talla': prodInfo.talla || '',
                        'PVP': prodInfo.pvp || 0,
                        'Descripción': prodInfo.descripcion || '',
                        'Total': item.totalSolicitado
                    });
                });
            });

            // Ordenar por ubicación alfabéticamente
            hojaRuta.sort((a, b) => a['Ubicación'].localeCompare(b['Ubicación']));

            // Guardar en la orden
            orden.hojaRutaPicking = hojaRuta;
            
            mostrarToast('Hoja de ruta generada para Picking', 'success');
        }

        function renderizarOrdenes() {
            document.getElementById('ordenesTableBody').innerHTML = ordenes.map(orden => {
                const progreso = orden.estado === 'Creada' ? 0 : 
                                 orden.estado === 'En Picking' ? 33 :
                                 orden.estado === 'En Packing' ? 66 : 100;
                
                return `
                    <tr>
                        <td><strong>${orden.id}</strong></td>
                        <td>${orden.fecha.toLocaleDateString()}</td>
                        <td>${orden.totalUnidades}</td>
                        <td><span class="badge badge-blue">${orden.estado}</span></td>
                        <td>
                            <div class="progress-bar">
                                <div class="progress-fill" style="width: ${progreso}%"></div>
                            </div>
                        </td>
                        <td>
                            <button class="btn btn-outline" style="padding: 0.25rem 0.75rem; font-size: 0.875rem;" onclick="descargarHojaRuta('${orden.id}')">📥 Hoja Ruta</button>
                        </td>
                    </tr>
                `;
            }).join('');
        }

        function descargarHojaRuta(ordenId) {
            const orden = ordenes.find(o => o.id === ordenId);
            if (!orden.hojaRutaPicking) {
                mostrarToast('No hay hoja de ruta disponible', 'warning');
                return;
            }

            const ws = XLSX.utils.json_to_sheet(orden.hojaRutaPicking);
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, 'Hoja Ruta Picking');
            XLSX.writeFile(wb, `hoja-ruta-picking-${ordenId}.xlsx`);
            mostrarToast('Hoja de ruta descargada', 'success');
        }

        // PICKING - Confirmación de Cantidades
        function renderizarPicking() {
            const ordenesPicking = ordenes.filter(o => o.estado === 'Creada' || o.estado === 'En Picking');
            
            document.getElementById('pickingOrdenesContainer').innerHTML = ordenesPicking.map(orden => `
                <div class="card" style="margin-bottom: 1rem;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem;">
                        <div>
                            <h4><strong>${orden.id}</strong></h4>
                            <p style="color: var(--text-secondary); font-size: 0.875rem;">
                                Total: ${orden.totalUnidades} unidades | Estado: ${orden.estado}
                            </p>
                        </div>
                        <div style="display: flex; gap: 0.5rem;">
                            <button class="btn btn-outline" onclick="descargarHojaRuta('${orden.id}')">
                                📥 Descargar Hoja Ruta
                            </button>
                            <button class="btn btn-primary" onclick="subirCantidadesEncontradas('${orden.id}')">
                                📤 Subir Cantidades Encontradas
                            </button>
                        </div>
                    </div>
                    
                    ${orden.cantidadesEncontradas ? `
                        <div class="alert alert-success">
                            <strong>✓ Cantidades confirmadas</strong><br>
                            Encontradas: ${orden.unidadesEncontradas} de ${orden.totalUnidades} solicitadas
                            ${orden.unidadesFaltantes > 0 ? `<br><span style="color: var(--danger);">⚠ Faltantes: ${orden.unidadesFaltantes}</span>` : ''}
                        </div>
                        <button class="btn btn-success" onclick="confirmarPicking('${orden.id}')">
                            ✓ Confirmar y Bloquear Unidades
                        </button>
                    ` : ''}
                </div>
            `).join('') || '<p style="color: var(--text-secondary);">No hay órdenes pendientes de picking</p>';
        }

        function subirCantidadesEncontradas(ordenId) {
            const input = document.createElement('input');
            input.type = 'file';
            input.accept = '.xlsx,.xls';
            input.onchange = (e) => procesarCantidadesEncontradas(e, ordenId);
            input.click();
        }

        function procesarCantidadesEncontradas(event, ordenId) {
            const file = event.target.files[0];
            if (!file) return;

            mostrarToast('Procesando cantidades encontradas...', 'info');

            const reader = new FileReader();
            reader.onload = function(e) {
                try {
                    const data = new Uint8Array(e.target.result);
                    const workbook = XLSX.read(data, { type: 'array' });
                    const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
                    const jsonData = XLSX.utils.sheet_to_json(firstSheet);

                    const orden = ordenes.find(o => o.id === ordenId);
                    orden.cantidadesEncontradas = [];
                    let totalEncontrado = 0;

                    jsonData.forEach(row => {
                        const variante = String(row.Variante || row.variante);
                        const ubicacion = String(row.Ubicacion || row.ubicacion || row['Ubicación']).toUpperCase();
                        const cantidadEncontrada = parseInt(row['Cantidad Encontrada'] || row.cantidadEncontrada || 0);

                        orden.cantidadesEncontradas.push({
                            variante,
                            ubicacion,
                            cantidadEncontrada
                        });

                        totalEncontrado += cantidadEncontrada;
                    });

                    orden.unidadesEncontradas = totalEncontrado;
                    orden.unidadesFaltantes = orden.totalUnidades - totalEncontrado;
                    orden.estado = 'En Picking';

                    mostrarToast('Cantidades encontradas cargadas correctamente', 'success');
                    renderizarPicking();
                    renderizarOrdenes();

                } catch (error) {
                    console.error(error);
                    mostrarToast('Error al procesar archivo', 'danger');
                }
            };
            reader.readAsArrayBuffer(file);
        }

        function confirmarPicking(ordenId) {
            const orden = ordenes.find(o => o.id === ordenId);
            
            if (!orden.cantidadesEncontradas) {
                mostrarToast('Primero debes subir las cantidades encontradas', 'warning');
                return;
            }

            // Bloquear unidades en inventario
            orden.cantidadesEncontradas.forEach(item => {
                const invItem = inventario.find(inv => 
                    inv.variante === item.variante && inv.ubicacion === item.ubicacion
                );
                if (invItem) {
                    invItem.stockBloqueado += item.cantidadEncontrada;
                }
            });

            // Redistribuir proporcional si hay faltantes
            if (orden.unidadesFaltantes > 0) {
                redistribuirOrdenProporcional(orden);
            }

            orden.estado = 'Confirmado - Listo para Packing';
            
            // Generar hoja para Packing
            generarHojaPacking(orden);

            mostrarToast(`Unidades bloqueadas. Orden lista para Packing.`, 'success');
            renderizarPicking();
            renderizarPacking();
            renderizarOrdenes();
            actualizarDashboard();
            guardarDatos(); // ✅ GUARDAR CAMBIOS
        }

        function redistribuirOrdenProporcional(orden) {
            const factorReduccion = orden.unidadesEncontradas / orden.totalUnidades;

            orden.items.forEach(item => {
                Object.keys(item.distribucion).forEach(tienda => {
                    const cantidadOriginal = item.distribucion[tienda];
                    item.distribucion[tienda] = Math.floor(cantidadOriginal * factorReduccion);
                });
            });

            orden.distribucionAjustada = true;
            orden.totalUnidades = orden.unidadesEncontradas;
        }

        function generarHojaPacking(orden) {
            const hojaPacking = [];

            orden.items.forEach(item => {
                const prodInfo = productosSystem.find(p => p.variante === item.variante) || {};
                
                const fila = {
                    'Variante': item.variante,
                    'Código Comercial': prodInfo.codigoComercial || '',
                    'Descripción': prodInfo.descripcion || '',
                    'Marca': prodInfo.marca || '',
                    'Talla': prodInfo.talla || '',
                    'PVP': prodInfo.pvp || 0
                };

                // Agregar distribución por tienda
                TIENDAS_LUKERS.forEach(tienda => {
                    fila[tienda] = item.distribucion[tienda] || 0;
                });

                fila['Total'] = Object.values(item.distribucion).reduce((sum, val) => sum + val, 0);
                hojaPacking.push(fila);
            });

            orden.hojaPacking = hojaPacking;
        }

        // PACKING - Observaciones y Cierre
        function renderizarPacking() {
            const ordenesPacking = ordenes.filter(o => 
                o.estado === 'Confirmado - Listo para Packing' || 
                o.estado === 'En Packing'
            );
            
            document.getElementById('packingOrdenesContainer').innerHTML = ordenesPacking.map(orden => `
                <div class="card" style="margin-bottom: 1rem;">
                    <div style="display: flex; justify-content: space-between; align-items: center; margin-bottom: 1rem;">
                        <div>
                            <h4><strong>${orden.id}</strong></h4>
                            <p style="color: var(--text-secondary); font-size: 0.875rem;">
                                Total: ${orden.totalUnidades} unidades
                                ${orden.distribucionAjustada ? '<span class="badge badge-yellow">Redistribuido</span>' : ''}
                            </p>
                        </div>
                        <div style="display: flex; gap: 0.5rem;">
                            <button class="btn btn-outline" onclick="descargarHojaPacking('${orden.id}')">
                                📥 Descargar Hoja Packing
                            </button>
                            <button class="btn btn-primary" onclick="reportarObservaciones('${orden.id}')">
                                📝 Reportar Observaciones
                            </button>
                        </div>
                    </div>
                    
                    ${orden.observaciones ? `
                        <div class="alert alert-warning">
                            <strong>Observaciones reportadas:</strong><br>
                            Prendas rechazadas: ${orden.prendasRechazadas || 0}
                        </div>
                        <button class="btn btn-success" onclick="cerrarOrdenPacking('${orden.id}')">
                            ✓ Cerrar Orden y Finalizar
                        </button>
                    ` : ''}
                </div>
            `).join('') || '<p style="color: var(--text-secondary);">No hay órdenes en packing</p>';
        }

        function descargarHojaPacking(ordenId) {
            const orden = ordenes.find(o => o.id === ordenId);
            if (!orden.hojaPacking) {
                mostrarToast('No hay hoja de packing disponible', 'warning');
                return;
            }

            const ws = XLSX.utils.json_to_sheet(orden.hojaPacking);
            const wb = XLSX.utils.book_new();
            XLSX.utils.book_append_sheet(wb, ws, 'Hoja Packing');
            XLSX.writeFile(wb, `hoja-packing-${ordenId}.xlsx`);
            mostrarToast('Hoja de packing descargada', 'success');
        }

        function reportarObservaciones(ordenId) {
            const input = document.createElement('input');
            input.type = 'file';
            input.accept = '.xlsx,.xls';
            input.onchange = (e) => procesarObservacionesPacking(e, ordenId);
            input.click();
        }

        function procesarObservacionesPacking(event, ordenId) {
            const file = event.target.files[0];
            if (!file) return;

            mostrarToast('Procesando observaciones...', 'info');

            const reader = new FileReader();
            reader.onload = function(e) {
                try {
                    const data = new Uint8Array(e.target.result);
                    const workbook = XLSX.read(data, { type: 'array' });
                    const firstSheet = workbook.Sheets[workbook.SheetNames[0]];
                    const jsonData = XLSX.utils.sheet_to_json(firstSheet);

                    const orden = ordenes.find(o => o.id === ordenId);
                    orden.observaciones = [];
                    let totalRechazadas = 0;

                    jsonData.forEach(row => {
                        const variante = String(row.Variante || row.variante);
                        const cantidad = parseInt(row.Cantidad || row.cantidad || 0);
                        const motivo = String(row.Motivo || row.motivo || '').toUpperCase();

                        const observacion = {
                            variante,
                            cantidad,
                            motivo,
                            procesado: false
                        };

                        orden.observaciones.push(observacion);
                        totalRechazadas += cantidad;

                        // Crear item para reclasificación
                        const itemReclasificacion = {
                            id: `RECLA-${Date.now()}-${Math.random().toString(36).substr(2, 9)}`,
                            ordenId: ordenId,
                            varianteOriginal: variante,
                            cantidad,
                            motivo,
                            estado: 'Pendiente',
                            ubicacionDestino: motivo === 'MAL ESTADO' ? obtenerUbicacion191() : null,
                            nuevaVariante: null
                        };

                        itemsReclasificacion.push(itemReclasificacion);
                    });

                    orden.prendasRechazadas = totalRechazadas;
                    orden.estado = 'En Packing';

                    mostrarToast(`${totalRechazadas} prendas en reclasificación`, 'success');
                    renderizarPacking();
                    renderizarReclasificacion();

                } catch (error) {
                    console.error(error);
                    mostrarToast('Error al procesar observaciones', 'danger');
                }
            };
            reader.readAsArrayBuffer(file);
        }

        function obtenerUbicacion191() {
            // Buscar ubicación 191 disponible o crear nueva
            const ubicaciones191 = inventario
                .filter(inv => inv.ubicacion.startsWith('191'))
                .map(inv => inv.ubicacion);

            if (ubicaciones191.length === 0) {
                return '191-01-01';
            }

            // Retornar ubicación 191 genérica
            return '191-MAL-ESTADO';
        }

        function cerrarOrdenPacking(ordenId) {
            const orden = ordenes.find(o => o.id === ordenId);

            if (!orden.observaciones) {
                if (!confirm('No hay observaciones reportadas. ¿Deseas cerrar la orden sin observaciones?')) {
                    return;
                }
            }

            // Desbloquear y restar del inventario
            orden.cantidadesEncontradas.forEach(item => {
                const invItem = inventario.find(inv => 
                    inv.variante === item.variante && inv.ubicacion === item.ubicacion
                );
                if (invItem) {
                    invItem.stockBloqueado -= item.cantidadEncontrada;
                    invItem.stockFisico -= item.cantidadEncontrada;
                }
            });

            orden.estado = 'Completada';
            orden.fechaCierre = new Date();

            mostrarToast(`Orden ${ordenId} completada exitosamente`, 'success');
            renderizarPacking();
            renderizarOrdenes();
            actualizarDashboard();
            renderizarInventario();
            guardarDatos(); // ✅ GUARDAR CAMBIOS
        }

        // RECLASIFICACIÓN
        function renderizarReclasificacion() {
            document.getElementById('reclasificacionTableBody').innerHTML = 
                itemsReclasificacion.map(item => {
                    const esMalEstado = item.motivo === 'MAL ESTADO';
                    
                    return `
                        <tr>
                            <td><strong>${item.varianteOriginal}</strong></td>
                            <td>
                                <span class="badge badge-${esMalEstado ? 'red' : 'yellow'}">
                                    ${item.motivo}
                                </span>
                            </td>
                            <td>${item.cantidad}</td>
                            <td>
                                ${item.nuevaVariante || 
                                  (esMalEstado ? '<span style="color: var(--text-secondary);">Mantiene variante</span>' : 
                                  '<input type="text" class="form-control" id="nuevaVariante_${item.id}" placeholder="Nuevo código" style="width: 150px;">')}
                            </td>
                            <td>
                                ${item.ubicacionDestino || 
                                  (esMalEstado ? '<strong style="color: var(--danger);">191-MAL-ESTADO</strong>' : 
                                  '<input type="text" class="form-control" id="nuevaUbicacion_${item.id}" placeholder="Nueva ubicación" style="width: 150px;">')}
                            </td>
                            <td>
                                <span class="badge badge-${item.estado === 'Procesado' ? 'green' : 'yellow'}">
                                    ${item.estado}
                                </span>
                            </td>
                            <td>
                                ${item.estado === 'Pendiente' ? `
                                    <button class="btn btn-success" style="padding: 0.25rem 0.75rem; font-size: 0.875rem;" 
                                            onclick="procesarReclasificacion('${item.id}')">
                                        ✓ Procesar
                                    </button>
                                ` : '✓ Completado'}
                            </td>
                        </tr>
                    `;
                }).join('') || 
                '<tr><td colspan="7" style="text-align: center; color: var(--text-secondary);">No hay items pendientes de reclasificación</td></tr>';
        }

        function procesarReclasificacion(itemId) {
            const item = itemsReclasificacion.find(i => i.id === itemId);
            
            if (item.motivo === 'MAL ESTADO') {
                // Mal estado va directo a ubicación 191
                item.ubicacionDestino = '191-MAL-ESTADO';
                item.nuevaVariante = item.varianteOriginal; // Mantiene la misma variante
                
                // Agregar al inventario
                const existente = inventario.find(inv => 
                    inv.variante === item.nuevaVariante && inv.ubicacion === item.ubicacionDestino
                );
                
                if (existente) {
                    existente.stockFisico += item.cantidad;
                } else {
                    inventario.push({
                        variante: item.nuevaVariante,
                        ubicacion: item.ubicacionDestino,
                        stockFisico: item.cantidad,
                        stockBloqueado: 0
                    });
                }

                item.estado = 'Procesado';
                mostrarToast(`${item.cantidad} unidades reclasificadas a MAL ESTADO`, 'success');
                
            } else {
                // Otros motivos necesitan nueva variante y ubicación
                const nuevaVarianteInput = document.getElementById(`nuevaVariante_${itemId}`);
                const nuevaUbicacionInput = document.getElementById(`nuevaUbicacion_${itemId}`);
                
                if (!nuevaVarianteInput || !nuevaUbicacionInput) {
                    mostrarToast('Error al obtener datos', 'danger');
                    return;
                }

                const nuevaVariante = nuevaVarianteInput.value.trim();
                const nuevaUbicacion = nuevaUbicacionInput.value.trim().toUpperCase();

                if (!nuevaVariante || !nuevaUbicacion) {
                    mostrarToast('Debes ingresar la nueva variante y ubicación', 'warning');
                    return;
                }

                item.nuevaVariante = nuevaVariante;
                item.ubicacionDestino = nuevaUbicacion;

                // Agregar al inventario con nueva variante
                const existente = inventario.find(inv => 
                    inv.variante === nuevaVariante && inv.ubicacion === nuevaUbicacion
                );
                
                if (existente) {
                    existente.stockFisico += item.cantidad;
                } else {
                    inventario.push({
                        variante: nuevaVariante,
                        ubicacion: nuevaUbicacion,
                        stockFisico: item.cantidad,
                        stockBloqueado: 0
                    });
                }

                item.estado = 'Procesado';
                mostrarToast(`${item.cantidad} unidades reclasificadas con nueva variante ${nuevaVariante}`, 'success');
            }

            renderizarReclasificacion();
            renderizarInventario();
            actualizarDashboard();
            guardarDatos(); // ✅ GUARDAR CAMBIOS
        }

        // Actualizar renderizado al cambiar de vista
        function cambiarVista(vista) {
            document.querySelectorAll('.view-section').forEach(v => v.classList.remove('active'));
            document.getElementById(`view-${vista}`).classList.add('active');
            document.querySelectorAll('.nav-item').forEach(n => n.classList.remove('active'));
            document.querySelector(`[data-view="${vista}"]`)?.classList.add('active');
            document.getElementById('pageTitle').textContent = vista.charAt(0).toUpperCase() + vista.slice(1).replace(/-/g, ' ');
            
            // Renderizar según vista
            if (vista === 'picking') renderizarPicking();
            if (vista === 'packing') renderizarPacking();
            if (vista === 'reclasificacion') renderizarReclasificacion();
            if (vista === 'productos-system') renderizarProductosSystem();
        }

        // Inicializar al cargar
        document.addEventListener('DOMContentLoaded', init);
    </script>
</body>
</html>
