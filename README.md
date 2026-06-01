# 📚 SIGPA — Sistema Integral de Gestión de Prácticas Académicas

Sistema desarrollado para centralizar, automatizar y realizar el seguimiento del proceso de prácticas pedagógicas de los estudiantes de licenciatura de la UDI, conforme al Decreto 1075 de 2015 del MEN.

---

## 👥 Integrantes

| Nombre | Rol |
|---|---|
| Jorge Enrique Saldaña Gómez | Estudiante Ing. Sistemas |
| Juan Felipe Gutierrez Galvis | Estudiante Ing. Sistemas |
| Alonso Andres Henao Roa | Estudiante Ing. Sistemas |

**Universidad de Investigación y Desarrollo (UDI) — Bucaramanga**  
**Proyecto Integrador · Semestre I – 2026**

---

## 📌 Estado del Proyecto

🟢 **Finalizado — Fase 3 completada:** Software funcional al 100 % de los casos de uso.

> **⚡ Todo el proyecto final (código fuente, base de datos, documentación y diagramas) se encuentra en la carpeta [`entrega_final/`](./entrega_final).**

---

## 📋 Descripción

En los programas de licenciatura de la UDI, la gestión de las prácticas pedagógicas se realizaba de forma dispersa mediante correos electrónicos, hojas de cálculo y archivos físicos, lo que generaba sobrecarga administrativa, riesgo de pérdida de evidencias y falta de trazabilidad.

SIGPA resuelve ese problema centralizando en un solo entorno los **8 niveles de práctica pedagógica**, permitiendo:

- Asignación eficiente de plazas por parte del Director.
- Registro y seguimiento de bitácoras y evidencias en tiempo real por los estudiantes.
- Supervisión y retroalimentación del Docente Asesor.
- Aprobación de instituciones receptoras por el Coordinador de Prácticas.
- Control de horas de práctica (hasta 50 h reglamentarias).
- Generación de reportes por grupo de práctica.

---

## 🗂️ Estructura del Repositorio

```
SIGPA/
│
├── entrega_final/            ⬅️  PROYECTO FINAL COMPLETO
│   ├── codigo_fuente/        →  Proyecto Java (NetBeans) con todas las clases
│   ├── base_de_datos/        →  Script SQL, diccionario de datos, modelos E-R y relacional
│   ├── documentacion/        →  Documento del proyecto, SRS, manuales y artículo IEEE
│   └── diagramas/            →  Diagramas UML (casos de uso, secuencia, clases, dominio,
│                                 componentes y despliegue) — Astah
│
├── base_de_datos/            →  Avances anteriores de BD
├── diagramas_ing_software/   →  Avances anteriores de diagramas
├── documentacion/            →  Avances anteriores de documentación
├── prototipo_java/           →  Prototipo funcional (Fase 2)
└── README.md
```

---

## 🛠️ Tecnologías Utilizadas

| Componente | Tecnología |
|---|---|
| Lenguaje de programación | Java |
| Interfaz gráfica | Java Swing |
| Base de datos | Oracle SQL\*Plus (esquema `SIGPAJFA`) |
| Entorno de desarrollo | NetBeans IDE |
| Modelado UML | Astah |
| Control de versiones | Git / GitHub |

---

## 🗄️ Base de Datos

El esquema relacional `SIGPAJFA` contiene 11 tablas:

| # | Tabla | Descripción |
|---|---|---|
| 1 | `USUARIO` | Tabla base con datos comunes a todos los roles |
| 2 | `DIRECTOR` | Datos del director del programa (hereda de Usuario) |
| 3 | `DOCENTE_ASESOR` | Datos del docente que supervisa prácticas |
| 4 | `ESTUDIANTE` | Datos académicos del practicante |
| 5 | `COORD_PRACTICA` | Coordinador que gestiona instituciones |
| 6 | `INSTITUCION` | Instituciones receptoras con convenio activo |
| 7 | `GRUPO_PRACTICA` | Grupos por nivel, modalidad y sede |
| 8 | `PRACTICA` | Tabla central que relaciona estudiante, docente, institución y grupo |
| 9 | `BITACORA` | Registro de visitas, evidencias y retroalimentación |
| 10 | `PREGUNTA` | Preguntas asociadas a cada bitácora |
| 11 | `REPORTE` | Reportes generados por grupo de práctica |

El script completo de creación se encuentra en `entrega_final/base_de_datos/`.

---

## 🖥️ Pantallas Principales

- **Login** — Autenticación por usuario/contraseña con validación de rol.
- **Menú Principal** — Navegación según el rol del usuario.
- **Gestión de Instituciones** — CRUD de instituciones receptoras y convenios.
- **Gestión de Usuarios** — Registro y administración por roles (Director, Docente, Estudiante, Coordinador).
- **Bitácoras** — Registro de visitas, respuesta a preguntas y carga de evidencias (link de Drive).
- **Control de Horas** — Contador de horas de práctica con progreso visual.
- **Reportes** — Generación de reportes por grupo y período académico.

---

## ⚙️ Requisitos para Ejecutar

- **Java JDK 8** o superior instalado.
- **Oracle Database** con acceso al esquema `SIGPAJFA` (o servidor de la Universidad).
- **NetBeans IDE** (recomendado para abrir el proyecto).
- Mínimo 4 GB de RAM y procesador de gama media.

### Pasos rápidos

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/ahenao2-hub/SIGPA.git
   ```
2. Abrir el proyecto desde `entrega_final/codigo_fuente/` en NetBeans.
3. Ejecutar el script SQL de `entrega_final/base_de_datos/` en Oracle SQL\*Plus para crear las tablas.
4. Configurar la conexión JDBC en el proyecto apuntando al esquema `SIGPAJFA`.
5. Ejecutar la clase principal del proyecto.

---

## 📄 Documentación

Toda la documentación final se encuentra en `entrega_final/documentacion/` e incluye:

- Documento del Proyecto Integrador (avances I, II y III).
- Plantilla SRS (Especificación de Requerimientos de Software) — ISO/IEC/IEEE 29148.
- Diccionario de datos.
- Manuales técnico y de usuario.
- Artículo final en formato IEEE.

---

## 📐 Diagramas UML

Disponibles en `entrega_final/diagramas/` (archivos `.astah` y capturas):

- Diagramas de Casos de Uso (Director, Estudiante, Docente Asesor, Coordinador, Institución Receptora).
- Diagrama de Dominio.
- Diagrama de Clases.
- Diagramas de Secuencia.
- Diagrama de Componentes.
- Diagrama de Despliegue.

---

## 📜 Normativa de Referencia

- **Decreto 1075 de 2015** — Ministerio de Educación Nacional (MEN).
- **Lineamientos CNA** para acreditación de alta calidad.
- **ISO/IEC/IEEE 29148** — Estándar para especificación de requisitos (SRS).
- **ISO 12207** — Procesos del ciclo de vida del software.

---

## 📝 Licencia

Proyecto académico — Universidad de Investigación y Desarrollo (UDI), 2026.
