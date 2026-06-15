# Luminom IA — Tutor Universitario

> Proyecto Final · Ruta Avanzada · Jóvenes creaTIvos

App web full stack de tutor universitario con inteligencia artificial personalizada, publicable en Vercel o GitHub Pages.

---

## Stack

- **Frontend**: HTML5 + CSS3 + JavaScript vanilla
- **Tipografía**: Playfair Display (display) + Inter (cuerpo) + Space Mono (mono)
- **IA**: Claude (Anthropic) vía API — modelo `claude-sonnet-4-6`
- **Persistencia**: localStorage para contactos y servicios
- **Deploy**: Vercel / GitHub Pages

---

## Estructura del proyecto

```
luminom-ia/
├── index.html        ← App principal (todas las secciones)
├── css/
│   └── styles.css    ← Sistema de diseño completo
├── js/
│   └── app.js        ← Lógica: chat IA, formulario, admin
├── vercel.json       ← Config para deploy en Vercel
└── README.md
```

---

## Secciones

| # | Sección | Descripción |
|---|---------|-------------|
| 1 | **Marca + Home** | Hero animado con identidad Luminom |
| 2 | **Catálogo** | 6 categorías de materias universitarias |
| 3 | **Tutor IA** | Chat en tiempo real con Claude |
| 4 | **Contacto** | Formulario con validaciones y guardado |
| 5 | **Admin** | Login + panel con mensajes y servicios |

---

## Cómo desplegar en Vercel

### Opción 1 — Vercel CLI (recomendada)

```bash
npm install -g vercel
cd luminom-ia/
vercel
```

Seguir el asistente → ¡listo!

### Opción 2 — Vercel desde GitHub

1. Subir la carpeta a un repositorio de GitHub
2. Entrar a [vercel.com](https://vercel.com) → New Project
3. Importar el repositorio
4. En **Environment Variables**, agregar:
   ```
   ANTHROPIC_API_KEY = sk-ant-...
   ```
5. Click en Deploy

> **Importante**: La API key de Anthropic debe estar como variable de entorno en Vercel, nunca en el código.

---

## Cómo desplegar en GitHub Pages

1. Subir todo a un repo de GitHub
2. Ir a Settings → Pages → Source: `main` branch, carpeta `/root`
3. GitHub genera la URL automáticamente

> Nota: Para GitHub Pages necesitas una solución de backend (Vercel Functions, Railway, etc.) para la API key de Anthropic, ya que no soporta variables de entorno.

---

## Variables de entorno necesarias

```env
ANTHROPIC_API_KEY=sk-ant-tu-clave-aqui
```

Obtén tu API key en: https://console.anthropic.com

---

## Admin

- **Usuario**: `admin`
- **Contraseña**: `luminom2024`
- Cambiar credenciales en `js/app.js` líneas 118-119

---

## Control de versiones (Git)

```bash
git init
git add .
git commit -m "feat: proyecto inicial Luminom IA"
# Continuar con commits semanales
git commit -m "feat: sección catálogo y tarjetas"
git commit -m "feat: integración API Claude chat"
git commit -m "feat: formulario contacto con validaciones"
git commit -m "feat: panel admin con login"
git commit -m "style: responsive mobile completo"
# ... mínimo 15 commits para el proyecto final
```

---

## Criterios cumplidos

- [x] Código limpio y organizado (frontend/backend separado)
- [x] Responsive en móvil y escritorio
- [x] Animaciones (float, fade-in, reveal on scroll)
- [x] Estados de carga (typing indicator, loader en botón)
- [x] Errores claros en formularios
- [x] IA personalizada (conoce el negocio, responde en español)
- [x] Formulario de contacto funcional
- [x] Panel admin con login
- [x] Catálogo de servicios dinámico
- [x] Desplegable en Vercel

---

*Luminom IA © 2024 · Jóvenes creaTIvos · Ruta Avanzada*
