# 🎯 Aura — Control de asistencia por QR

> Sistema web para **crear eventos, registrar asistentes con código QR y obtener
> estadísticas y reportes al instante.** En uso en la **Universidad de La Guajira**.

🔗 **Demo en vivo:** [asistencia.desarrollougmaicao.com](https://asistencia.desarrollougmaicao.com)

`Laravel` · `React (islas)` · `TypeScript` · `Tailwind` · `MySQL` · `Docker`

<!-- 📸 Agregar aquí 2–3 capturas: landing, panel de estadísticas, registro por QR.
     (Usá DevTools → clic derecho en el elemento → "Capture node screenshot" a DPR 2–3,
      y optimizá en squoosh.app. Guardá en /screenshots.) -->
![Panel de estadísticas](screenshots/dashboard.png)

---

## El problema
Las universidades registran la asistencia a eventos (charlas, talleres, actos) de forma
manual: listas en papel, conteos a mano, cero trazabilidad y reportes que tardan días.
No hay evidencia confiable ni estadísticas para tomar decisiones.

## La solución
Aura digitaliza todo el flujo, con evidencia y estadísticas en tiempo real:

- **📅 Gestión de eventos** — creación, cierre y administración de eventos por sede.
- **📲 Registro por QR** — el asistente se registra escaneando un código; captura datos
  demográficos (programa, tipo de participante, dependencia) sin filas ni papel.
- **📊 Estadísticas en vivo** — asistencias, participantes y eventos, con gráficas
  interactivas y comparación entre eventos.
- **📄 Reportes en PDF** — actas de asistencia generadas al instante.
- **🏢 Multi-sede** — aislamiento de datos por sede desde la arquitectura.
- **📥 Importación masiva** — carga asíncrona de participantes con revisión previa.
- **🔔 Notificaciones** in-app y por correo · **🛡️ RBAC** (roles y permisos granulares).

## Decisiones técnicas destacadas
- **Arquitectura multi-sede** con aislamiento de datos por *scope* (un servicio central
  garantiza que cada sede solo ve lo suyo).
- **Islas de React sobre Laravel** — el backend sirve HTML rápido (bueno para carga y SEO)
  y las secciones interactivas (estadísticas) montan componentes React puntuales.
- **PDF con mapeo de coordenadas** — las actas se rellenan sobre plantillas oficiales.
- **Cumplimiento de datos (Ley 1581)** — consentimiento persistido (fecha, IP, versión de
  la política) en el registro por QR, ya que se manejan datos de personas.
- **~25 endpoints de estadísticas** y una suite de **73 archivos de pruebas**.

## Resultados
Usado en eventos reales de la Universidad de La Guajira — cientos de asistentes registrados
por QR, con **~96 % de registro digital** y reportes generados en el momento.

## Mi rol
Diseño y desarrollo **full-stack**: arquitectura multi-sede, backend en Laravel, las islas de
React para estadísticas, generación de PDF, el flujo de QR y el módulo de cumplimiento de datos.

---

> 🔒 **Código fuente privado** (es un producto en uso). Disponible para revisión en una
> entrevista técnica o bajo pedido. Este repositorio es el *case study*; el demo en vivo está
> arriba.

**Contacto:** [LinkedIn](https://www.linkedin.com/in/) · kevinhafiddiazgarcia@gmail.com
