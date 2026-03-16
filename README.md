# 📊 Diagrama C4 - Sistema de Pedidos en Línea

Arquitectura completa de un **sistema de pedidos en línea** usando **Microservicios**, **Patrones de Diseño** y **Event-Driven Architecture**.

## 🚀 Acceso Rápido

### 🌐 **Ver Diagramas en GitHub Pages**
👉 **[Ver en GitHub Pages](https://tu-usuario.github.io/nombre-repo)**

### 📚 **Documentación**
- **[📋 Diagrama C4 Completo](documentos/DIAGRAMA_C4_COMPLETO.md)** - Descripción detallada de todos los niveles del C4
- **[🎯 Justificación Arquitectónica](documentos/JUSTIFICACION_ARQUITECTONICA.md)** - Decisiones y trade-offs
- **[💻 Ejemplos de Código](documentos/EJEMPLOS_CODIGO.md)** - Implementación de patrones
- **[📊 Resumen Ejecutivo](documentos/RESUMEN_EJECUTIVO.md)** - Visión general ejecutiva
- **[📐 PlantUML Diagrams](diagramas/C4_DIAGRAMS.puml)** - Diagramas en PlantUML

---

## 🏗️ Arquitectura de Alto Nivel

### **Niveles del Diagrama C4**

```
┌─────────────────────────────────────┐
│   NIVEL 1: Contexto                 │
│  (Usuarios, Sistema, Externos)      │
└─────────────────────────────────────┘
                ↓
┌─────────────────────────────────────┐
│   NIVEL 2: Contenedores             │
│  (6 Microservicios Principales)     │
└─────────────────────────────────────┘
                ↓
┌─────────────────────────────────────┐
│   NIVEL 3: Componentes              │
│  (Factory, Strategy, Observer)      │
└─────────────────────────────────────┘
```

### **Microservicios**

| Servicio | Propósito | Patrón |
|----------|-----------|--------|
| **API Gateway** | Punto de entrada, autenticación | Reverse Proxy |
| **Usuarios** | Registro, autenticación | Repository |
| **Pedidos** | Gestión de pedidos | Observer + Events |
| **Pagos** | Procesar pagos | Factory + Strategy |
| **Inventario** | Gestión de stock | Observer + Cache |
| **Notificaciones** | Envío de emails | Subscriber |

---

## 🎨 Patrones de Diseño

### **1. Factory Pattern** (Servicio de Pagos)
Crea procesadores de pago dinámicamente sin modificar código existente.

### **2. Strategy Pattern** (Procesadores)
Cada procesador es intercambiable e independiente.

### **3. Observer Pattern** (Pedidos)
Múltiples observadores reaccionan automáticamente a eventos.

### **4. Repository Pattern**
Abstrae el acceso a datos (PostgreSQL).

### **5. Event-Driven Architecture**
Desacoplamiento mediante RabbitMQ.

---

## ✅ Requisitos Cumplidos

### **Funcionales**
- ✅ Registrar usuario
- ✅ Crear pedido
- ✅ Procesar pago
- ✅ Actualizar inventario
- ✅ Enviar notificación

### **No Funcionales**
- ✅ Sistema escalable (microservicios)
- ✅ Módulos independientes (APIs)
- ✅ Fácil agregar nuevos pagos (Factory Pattern)
- ✅ Sistema reactivo (Event-Driven + Observer)

---

## 📁 Estructura del Proyecto

```
├── docs/                           # GitHub Pages
│   └── index.html                 # Página principal
│
├── documentos/                     # Documentación técnica
│   ├── DIAGRAMA_C4_COMPLETO.md
│   ├── JUSTIFICACION_ARQUITECTONICA.md
│   ├── EJEMPLOS_CODIGO.md
│   └── RESUMEN_EJECUTIVO.md
│
├── diagramas/                      # Diagramas en PlantUML
│   └── C4_DIAGRAMS.puml
│
├── README.md                       # Este archivo
└── .gitignore
```

---

## 🚀 Cómo Usar

### **Visualizar en GitHub Pages**
1. Fork este repositorio
2. Habilita GitHub Pages en Settings → Pages
3. Selecciona `/docs` como rama de publicación
4. Accede a `https://tu-usuario.github.io/nombre-repo`

### **Ver Diagramas en PlantUML Online**
1. Ve a https://www.plantuml.com/plantuml/uml/
2. Copia el contenido de `diagramas/C4_DIAGRAMS.puml`
3. Pega en el editor
4. ¡Visualiza!

---

## 💡 Beneficios de la Arquitectura

✨ **Escalabilidad** - Cada servicio escala independientemente
✨ **Modularidad** - Servicios con responsabilidades claras
✨ **Extensibilidad** - Fácil agregar nuevas funcionalidades
✨ **Resiliencia** - Fallos aislados
✨ **Desacoplamiento** - REST + AMQP
✨ **Testabilidad** - Componentes aislados

---

## 📞 Información

- **Versión:** 1.0
- **Última actualización:** Marzo 15, 2026
- **Licencia:** MIT

**¡El sistema está listo para crecer y escalar con el negocio!** 🚀