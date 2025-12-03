# Integración de IA con Google Gemini

## ¿Qué se ha implementado?

Se ha integrado **Google Gemini AI** al gestor de roadmap para análisis inteligente del proyecto. El sistema permite:

### Tipos de Análisis Disponibles:

1. **Resumen Ejecutivo** - Análisis general del estado del proyecto
2. **Identificar Riesgos** - Detecta desafíos y dependencias críticas
3. **Optimización** - Sugiere mejoras para acelerar entregas
4. **Análisis de Capacidad** - Evalúa si el equipo tiene suficientes recursos

## Cómo Configurar

### Paso 1: Obtener API Key de Google Gemini

1. Ve a [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Inicia sesión con tu cuenta de Google
3. Haz clic en "Create API Key"
4. Copia la clave generada

### Paso 2: Usar en la Aplicación

1. Abre el gestor de roadmap
2. Haz clic en el botón **"Analizar con IA"** (icono de ✨)
3. Pega tu API Key en el campo correspondiente
4. Selecciona el tipo de análisis que deseas
5. Haz clic en **"Analizar Roadmap"**

## Cómo Funciona

### Arquitectura:

```
┌─────────────────────┐
│  Roadmap Local      │
│  (Fases + Hitos)    │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│  Convierte a Texto  │
│  (Roadmap Summary)  │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────────────────┐
│  Google Gemini API              │
│  (Análisis Inteligente)         │
└──────────┬──────────────────────┘
           │
           ▼
┌──────────────────────────┐
│  Resultados del Análisis │
│  (Mostrados en Modal)    │
└──────────────────────────┘
```

### Prompts Usados:

Cada tipo de análisis usa un prompt específico:

- **Resumen**: Solicita estado general, hitos alcanzados y próximos pasos
- **Riesgos**: Identifica desafíos, dependencias críticas y áreas de preocupación
- **Optimización**: Sugiere mejoras de eficiencia y reducción de cuellos de botella
- **Capacidad**: Evalúa si hay suficientes recursos para los milestones

## API Key - Consideraciones de Seguridad

⚠️ **IMPORTANTE**: 

- La API Key se envía directamente desde tu navegador a Google Gemini API
- **NO se guarda** en la aplicación
- **NO se envía** a nuestros servidores
- Cada sesión requiere que ingreses la clave nuevamente
- Si compartes la API Key, otros pueden usarla para llamadas a Gemini

### Recomendaciones:

1. **Para desarrollo local**: Usa tu API Key personal (es seguro)
2. **Para producción**: 
   - Configura API Key a través de variables de entorno
   - Usa un servidor backend para manejar las llamadas
   - Implementa rate limiting y validaciones

## Ejemplo de Salida

**Tipo: Resumen Ejecutivo**
```
RESUMEN EJECUTIVO:

El roadmap de Luky se encuentra en fase inicial con un progreso general del 25%. 
Las fases principales son:

1. FASE 1 - Verificación y Riesgo (10 de Diciembre)
   Estado: EN PROGRESO
   
2. FASE 2 - Onboarding del Asesor (20 de Diciembre)
   Estado: PENDIENTE

Recomendaciones:
- Enfocarse en completar la automatización de DataCrédito
- Preparar ambiente para pruebas de QA
- Coordinar con equipo de onboarding...
```

## Limitaciones y Ventajas

### Ventajas:
✅ Análisis sin costo adicional (con plan gratuito de Gemini)
✅ Respuestas contextuales y personalizadas
✅ Identificación automática de riesgos
✅ Sugerencias de mejora inteligentes

### Limitaciones:
⚠️ Requiere conexión a internet
⚠️ Depende de la API de Google (disponibilidad)
⚠️ La API Key debe ser privada
⚠️ Limite de llamadas según plan de Google

## Alternativas y Extensiones Futuras

### Otras opciones de IA que podrías integrar:

1. **OpenAI API** (GPT-4)
   - Más potente pero con costo
   - Mayor flexibilidad en prompts
   
2. **Claude API** (Anthropic)
   - Excelente para análisis complejo
   - Interfaz clara y bien documentada

3. **Ollama** (Local)
   - Ejecutar IA localmente sin conexión
   - Privacidad total de datos

## Debugging

Si algo no funciona:

1. **Verifica la API Key**: Cópiala nuevamente desde Google AI Studio
2. **Revisa la consola** (F12 → Console) para ver errores específicos
3. **Comprueba conexión a internet**
4. **Valida que el roadmap tenga datos**: Sin milestones, los análisis son vacíos
5. **Revisa límites de API**: Si hiciste muchas llamadas, podría estar limitado

## Archivos Modificados

- `index.html` - Añadido modal de IA, funciones de integración con Gemini, cambio de colores PDF a formal (negro/gris)

## Próximas Mejoras

- [ ] Guardar análisis como PDF junto al roadmap
- [ ] Historial de análisis previos
- [ ] Soporte para múltiples modelos de IA
- [ ] Cache de resultados para evitar re-análisis
- [ ] Integración con backend para seguridad de API Keys
