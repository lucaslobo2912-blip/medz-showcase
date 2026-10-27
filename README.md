# MED.Z · Plataforma de estudio para la residencia médica

> Escaparate del proyecto. El código fuente es privado; aquí explico qué hace, cómo está construido y qué decisiones técnicas tomé.

🔗 **En producción:** [medz.app.br](https://medz.app.br) · Lanzamiento oficial: 1 de diciembre de 2026

## El problema

Quien estudia para la residencia médica hace clases, preguntas y exámenes antiguos en muchos lugares distintos, pero no sabe si está mejorando ni qué repasar. Planillas y cuadernos no aguantan el ritmo.

## La solución

MED.Z organiza toda la preparación en un solo lugar:

- **Rutina:** agenda semanal y mensual de exámenes, clases, bloques de preguntas y repasos
- **Registro de exámenes:** aciertos por gran área o por tema en menos de un minuto
- **Rendimiento:** evolución por área, por tema y por examen, con puntos fuertes y de atención
- **Repasos automáticos:** cada tema fallado genera un repaso en el día adecuado
- **Recordatorios:** en la plataforma y por e-mail, como máximo uno al día
- **Zaiko:** asistente que lee la rutina y los resultados del estudiante y propone el plan del día
- **Comunidad, soporte con tickets** y app instalable (PWA) en móvil y ordenador

## Arquitectura

| Capa | Tecnología |
|---|---|
| Frontend | Next.js, React, TypeScript, Tailwind CSS, Framer Motion |
| Backend | Cloudflare Workers (serverless), API REST propia |
| Datos | SQL (SQLite/D1) con migraciones versionadas |
| Pagos | Pasarela Asaas: suscripciones con tarjeta y PIX, webhooks verificados e idempotentes |
| E-mail | Resend: acceso, recuperación de contraseña y recordatorios |
| Anti-bots | Cloudflare Turnstile |

## Calidad

- **24 suites de tests automatizados** con base de datos real en memoria (autenticación, pagos, aislamiento entre cuentas y buenas prácticas de seguridad)
- Accesibilidad **WCAG 2.1 AA** verificada con axe-core en las páginas públicas
- Cumplimiento de la **LGPD** (equivalente brasileño del RGPD): política de privacidad, consentimiento de cookies y canal de derechos

## Mi papel

Idea, diseño de producto, UI, desarrollo full stack, seguridad, integraciones, lanzamiento y contenido de marketing. Desarrollo con apoyo de herramientas de IA (Codex, Claude) para entregar más rápido.

---

**Lucas Lobo** · lucaslobo2912@gmail.com · [GitHub](https://github.com/lucaslobo2912-blip)
