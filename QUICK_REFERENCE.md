# 🚀 REFERENCIA RÁPIDA - Comandos y Accesos

## 📍 Ubicaciones Importantes

### Gestor de Roadmap:
```
📁 c:\Users\Jeferson Camero\OneDrive\Escritorio\cash\cashblock-roadmap\
├── index.html (archivo principal)
├── GEMINI_AI_SETUP.md (setup de IA)
├── QUICK_START_IA.md (guía rápida)
├── README_v2.md (resumen de cambios)
├── ARCHITECTURE.md (diagramas técnicos)
└── CHANGELOG.md (detalles técnicos)
```

### Abrir en navegador:
```
Opción 1: Arrastra index.html al navegador
Opción 2: Haz clic derecho → Open with → Browser
Opción 3: Ctrl+O en navegador → selecciona index.html
```

---

## 🔑 Obtener API Key Gemini

```
1. Abre: https://aistudio.google.com/app/apikey
2. Clic en "Create API Key"
3. Se genera automáticamente
4. Copia (Ctrl+C)
5. Vuelve al gestor
6. Botón "Analizar con IA"
7. Pega en el campo
8. ¡Listo!
```

**Tiempo**: 1 minuto
**Costo**: $0
**Expira**: Solo si la borras

---

## 🎯 Acciones Principales

### Descargar PDF (Formal):
```
CLICK: Botón verde "Descargar PDF"
RESULTADO: PDF en colores gris/negro
UBICACIÓN: Tu carpeta Descargas
NOMBRE: roadmap-luky-YYYY-MM-DD.pdf
```

### Analizar con IA:
```
CLICK: Botón morado "Analizar con IA"
INPUT: 
  - Pega API Key
  - Selecciona tipo análisis
  - Clic "Analizar Roadmap"
ESPERA: 5-15 segundos
RESULTADO: Análisis en modal
```

### Ver Dashboard:
```
CLICK: Botón azul "Ver Dashboard"
MUESTRA: Métricas de desarrolladores
DATOS: Hitos y checklist completado por dev
```

---

## 📱 Botones del Header

| Botón | Color | Función | Nuevo |
|-------|-------|---------|-------|
| Descargar PDF | Verde | Genera PDF formal | No |
| Analizar con IA | Morado | Abre modal IA | **SÍ** |
| Restaurar Default | Rojo | Reinicia datos | No |
| Ver Dashboard | Azul | Métricas equipo | No |

---

## 🎨 Estructura del Modal IA

```
┌─ ENCABEZADO (Morado)
│  Título: "Análisis IA con Gemini"
│  Botón X para cerrar
│
├─ CONTENIDO
│  • Campo API Key (password)
│  • Link a aistudio.google.com
│  • Selector tipo análisis (4 opciones)
│  • Spinner de carga (oculto al inicio)
│  • Caja de resultados (oculta al inicio)
│
└─ BOTONES
   • Cancelar (gris)
   • Analizar Roadmap (morado)
```

---

## 4️⃣ Tipos de Análisis

### 1️⃣ Resumen Ejecutivo
```
¿Qué hace?
→ Estado general del proyecto
→ Hitos principales
→ Próximos pasos

Cuándo usar:
→ Presentaciones
→ Reportes gerenciales
→ Revisión general
```

### 2️⃣ Identificar Riesgos
```
¿Qué hace?
→ Desafíos potenciales
→ Dependencias críticas
→ Áreas de preocupación

Cuándo usar:
→ Planificación
→ Mitigación de riesgos
→ Análisis técnico
```

### 3️⃣ Optimización
```
¿Qué hace?
→ Sugerencias de mejora
→ Reducción de cuellos
→ Aceleración

Cuándo usar:
→ Mejorar velocidad
→ Eficiencia
→ Reducir tiempo
```

### 4️⃣ Capacidad del Equipo
```
¿Qué hace?
→ Evaluación de recursos
→ Viabilidad de timeline
→ Necesidades de personal

Cuándo usar:
→ Asignación de equipo
→ Planificación de hiring
→ Evaluación de carga
```

---

## 🔄 Flujo de Uso Típico

```
DÍA 1:
┌─ Abres gestor
├─ Actualizas fases/hitos
├─ Guardas en Firestore
└─ Cierras

DÍA 2:
┌─ Abres gestor
├─ Descarga PDF para reporte
├─ Analiza con IA (Resumen)
├─ Copia análisis
├─ Lo pega en documento
└─ Envía a equipo

DÍA 3:
┌─ Abres gestor
├─ Ve Dashboard (métricas)
├─ Analiza con IA (Riesgos)
├─ Identifica qué necesita mitigar
├─ Actualiza roadmap
└─ Guarda cambios
```

---

## 🛡️ Cosas Importantes

### ✅ SEGURO:
- Usar API Key en desarrollo local
- Cambiar API Key si la compartes
- Cada sesión necesita nueva API Key

### ❌ NO SEGURO:
- Poner API Key en código GitHub
- Compartir en chat o email
- Dejarla en logs públicos
- Usar en producción sin backend

### 🔒 SI LA COMPROMETISTE:
```
1. Ve a https://aistudio.google.com/app/apikey
2. Haz clic en 3 puntos de la clave
3. Selecciona "Delete"
4. Crea nueva clave
```

---

## 📊 Colores del PDF - Referencia

| Elemento | RGB Anterior | RGB Nuevo |
|----------|-------------|-----------|
| Título | (30,50,100) azul | (0,0,0) negro |
| Subtítulos | (100,100,100) gris claro | (80,80,80) gris oscuro |
| Líneas | (100,150,200) azul cielo | (40,40,40) gris oscuro |
| Completado | (34,197,94) verde | (60,60,60) gris |
| Pendiente | (245,158,11) naranja | (100,100,100) gris |

**Resultado**: Gama formal, monocromática, profesional

---

## 💾 Dónde se Guardan los Datos

```
Base de Datos: Google Firestore
└─ Proyecto: pivotal-cistern-479415-c4
   └─ Colección: roadmap
      └─ Documento: luky_roadmap_shared
         └─ Data: { db: [phases...] }
```

**Sincronización**: Automática cada vez que:
- Agregas/editas fase
- Agregas/editas hito
- Cambias estado
- Mueves orden
- Editas checklist

---

## 🐛 Troubleshooting

### Problema: "API Key inválida"
```
Solución:
1. Ve a https://aistudio.google.com/app/apikey
2. Genera nueva clave
3. Verifica que sea la correcta (tiene AIza...)
4. Pega de nuevo en modal
```

### Problema: "Sin respuesta de IA"
```
Solución:
1. Verifica conexión internet
2. Espera más (puede tardar 30 seg)
3. Intenta de nuevo
4. Revisa límite de llamadas (50/min)
```

### Problema: "No se descarga PDF"
```
Solución:
1. Verifica que el navegador permita descargas
2. Intenta en otra pestaña
3. Actualiza página (F5)
4. Usa otro navegador
```

### Problema: "Datos no se guardan"
```
Solución:
1. Verifica conexión a internet
2. Revisa que Firebase esté conectado
3. Abre consola (F12) para ver errores
4. Actualiza página
```

---

## 🔗 Enlaces Útiles

### Google Gemini:
- API Key: https://aistudio.google.com/app/apikey
- Documentación: https://ai.google.dev/

### Roadmap Manager:
- Archivo: c:\Users\Jeferson Camero\OneDrive\Escritorio\cash\cashblock-roadmap\index.html
- Git: (repository local)

### Documentación:
- Setup: GEMINI_AI_SETUP.md
- Quick Start: QUICK_START_IA.md
- Cambios: CHANGELOG.md
- Arquitectura: ARCHITECTURE.md
- Resumen: README_v2.md

---

## 🎓 Ejemplos de Prompts Personalizados

Si quieres análisis específico:

```
"¿Cuál es el hito más crítico?"
"¿Hay dependencias entre fases?"
"¿Podemos paralelizar algún trabajo?"
"¿Qué habilidades necesita el equipo?"
"¿Cuántos días quedan hasta el final?"
"¿Cuál es el riesgo más grande?"
```

Nota: Actualmente los 4 tipos predefinidos son fijos, pero el código está diseñado para extender fácilmente.

---

## 📋 Checklist de Configuración

```
□ Descargaste index.html
□ Obtuviste API Key de Google
□ Abriste index.html en navegador
□ Viste el botón "Analizar con IA"
□ Pegaste API Key en modal
□ Seleccionaste tipo de análisis
□ Ejecutaste análisis
□ Recibiste resultado
□ Descargaste PDF (nuevo formato gris)
□ ¡Listo para trabajar!
```

---

## 🚀 Próximos Pasos

1. Prueba analizar tu roadmap actual
2. Experimenta con los 4 tipos
3. Identifica insights útiles
4. Incorpora sugerencias de IA
5. Comparte análisis con equipo

---

**Última actualización**: 3 Diciembre 2025
**Versión**: 2.0
**Estado**: ✅ Listo
**Soporte**: Revisa archivos .md en la carpeta
