---
layout: post
title: "Formateando mi viejo Mac"
date: 2026-03-17
categories: [dev, mac, setup]
---

---

# 💻 Intentado revivir mi MacBook Pro de 2015

Durante años, mi **MacBook Pro** fue acumulando lo típico: aplicaciones instaladas y borradas, configuraciones olvidadas, archivos duplicados… y, en general, una buena capa de “ruido digital”.

El resultado: un equipo cada vez más lento, menos fiable y poco agradable para trabajar.

Así que decidí hacer lo que muchos evitamos durante años: **empezar de cero**.

Y lo interesante es que no solo recuperé el rendimiento… sino que poco a poco he ido construyendo un entorno de desarrollo **mucho más ligero que el original**.

Este artículo es el proceso completo.

---

# 🧹 Empezar de cero: la clave de todo

La decisión fue clara: **formateo completo e instalación limpia de macOS**.

Nada de migraciones, nada de restaurar copias antiguas. Solo:

* borrar disco
* reinstalar sistema
* empezar limpio

El cambio es inmediato:

* arranque mucho más rápido
* menos consumo de memoria
* sistema estable

Después de tantos años, el Mac literalmente “respira”.

---

# ☁️ iCloud como red de seguridad

Antes de borrar nada, verifiqué que todos mis documentos estaban correctamente sincronizados en **iCloud Drive**.

Esto es importante (sobre todo si sois un poco **paranóicos** como yo), no basta con que “parezca que está en la nube”. Hay que comprobarlo.

Gracias a esto pude formatear sin miedo. Al iniciar sesión después, todos los archivos volvieron automáticamente.

---

# ⚙️ Instalar solo lo necesario

Con el sistema limpio, había que optimizar rendimiento:

👉 instalar **solo lo imprescindible**

La herramienta base para esto es **Homebrew**, que permite instalar software desde terminal de forma rápida y controlada.

A partir de ahí, monté el entorno básico:

* **Git** para control de versiones
* **Node.js** para desarrollo web
* conexión con **GitHub** mediante SSH

Esto último es especialmente importante: una vez configurado, puedes trabajar sin introducir credenciales constantemente.

---

# ⚠️ No todo sale como planeamos

Apareció el primer obstáculo.

Intentar instalar Node con Homebrew en **macOS Monterey** implicaba compilar dependencias enormes (LLVM, Rust…), lo que en un Mac antiguo puede tardar horas… o directamente fallar.

La solución fue cambiar de enfoque:

👉 usar **nvm**

Esto tiene varias ventajas:

* evita compilaciones pesadas
* permite cambiar de versión fácilmente
* es más estable en sistemas antiguos

Una de esas decisiones que parecen pequeñas, pero cambian totalmente la experiencia.

---

# 🖥️ La terminal como centro de trabajo

En lugar de depender de interfaces gráficas, todo el flujo gira alrededor de:

* **iTerm2** → una terminal mucho más potente
* **Zsh** → el intérprete de comandos
* **Starship** → un prompt inteligente

Starship no cambia lo que haces… pero sí cómo lo ves.

Por ejemplo:

```
~/retro-lab 🌱 main ⬢ v20
❯
```

De un vistazo sabes:

* en qué carpeta estás
* en qué rama de git
* qué versión de Node usas
* si hay cambios sin guardar

---

# 🧠 Un editor ligero: menos es más

En lugar de usar entornos pesados, opté por **Sublime Text**.

Con algunos ajustes y plugins:

* resaltado de sintaxis
* autoformateo
* linting

consigue prácticamente lo mismo que un IDE moderno, pero con un consumo de recursos mínimo.

---

# ⚡ Automatización: el verdadero salto de productividad


Definí comandos personalizados en la terminal como:

```bash
newweb proyecto
serve
update
```

---

## Crear un proyecto en segundos

```bash
newweb calculadora
```

Esto automáticamente:

* crea la estructura de carpetas
* genera HTML, CSS y JS base
* inicializa git
* abre el proyecto

Sin escribir prácticamente nada.

---

## Servidor local instantáneo

```bash
serve
```

y ya tienes:

```
http://localhost:8000
```

sin instalar frameworks ni configuraciones complejas.

---

## Mantenimiento del sistema

```bash
update
```

mantiene el entorno limpio y actualizado.

---

# 📁 Finder + Terminal: pequeños detalles que importan

También integré el flujo con Finder:

* abrir terminal en una carpeta
* abrir proyectos directamente en el editor
* simplificar navegación

Aquí aprendí algo interesante: macOS no siempre gestiona bien los atajos de “Servicios”. A veces es más eficiente usar soluciones propias (alias, funciones, scripts).

---

# 🧩 Conclusión

No necesitas un equipo nuevo para programar bien (aunque te hace la vida mucho más fácil, evidentemente).

Con un sistema limpio, herramientas adecuadas y un poco de automatización, un portátil de hace más de 10 años puede convertirse en un entorno de desarrollo perfectamente válido para pequeños proyectos.

Iré contando cada proyecto que desarrolle, salga bien o mal, en este pequeño blog.

---
