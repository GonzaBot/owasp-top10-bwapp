# OWASP Top 10 — Explotación y análisis sobre bWAPP

Evaluación práctica de seguridad de aplicaciones web que documenta la explotación y el análisis de causa raíz de las diez categorías del **OWASP Top 10 (2021)**, realizada en un entorno de laboratorio aislado sobre la aplicación deliberadamente vulnerable bWAPP (BeeBox).

Cada ejercicio identifica la vulnerabilidad, demuestra su explotación, explica el fallo de fondo que la origina y, en los casos relevantes, lo aborda desde la perspectiva defensiva (detección y remediación).

## Vulnerabilidades cubiertas

| # | Categoría OWASP | Vulnerabilidad demostrada |
|---|---|---|
| A01 | Broken Access Control | Insecure Direct Object Reference (IDOR) |
| A02 | Cryptographic Failures | Hashing débil (SHA-1 sin salt) + cracking |
| A03 | Injection | SQL Injection (UNION-based) |
| A03 | Injection | Cross-Site Scripting (XSS) reflejado (GET/POST) |
| A04 | Insecure Design | Seguridad por oscuridad en autenticación |
| A05 | Security Misconfiguration | Local File Inclusion (LFI) / path traversal |
| A06 | Vulnerable & Outdated Components | Stored XSS (persistente) |
| A07 | Identification & Authentication Failures | Credenciales expuestas y sesión no invalidada |
| A09 | Security Logging & Monitoring Failures | Análisis de registros y ausencia de alertas |
| A10 | Server-Side Request Forgery | SSRF para escaneo de puertos interno |

## Enfoque

El objetivo no es solo explotar, sino entender. Para cada vulnerabilidad el informe distingue entre el síntoma (la explotación) y la causa (el error de diseño o implementación que la habilita), que es lo que determina cómo se corrige. El ejercicio de logging y monitoreo adopta directamente la perspectiva del analista defensivo, evaluando si la aplicación detecta y reacciona ante los ataques o se limita a registrarlos.

## Entorno

Todas las pruebas se realizaron en un laboratorio aislado, sin conexión a sistemas de terceros:

- **Aplicación objetivo:** bWAPP (buggy Web Application) sobre la máquina virtual BeeBox.
- **Herramientas:** navegador y herramientas de desarrollador, MySQL, John the Ripper.

> Las credenciales y datos que aparecen en el informe pertenecen exclusivamente a las cuentas de entrenamiento que bWAPP incluye por defecto. No se accedió a ningún sistema real ni a información de personas.

## Contenido del repositorio

```
.
├── Informe_OWASP_Top10.pdf     # Informe técnico completo con evidencias
└── README.md
```

## Herramientas

bWAPP / BeeBox · MySQL · John the Ripper · Navegador (DevTools)

## Autor

**Gonzalo Rodriguez** · [GitHub](https://github.com/GonzaBot) · [LinkedIn](https://www.linkedin.com/in/gonzardem)
