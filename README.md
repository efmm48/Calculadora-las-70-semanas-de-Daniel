# 📜 Las 70 Semanas de Daniel — 
Para abrir la aplicación haga clic en el enlace a la derecha -> [https://efmm48.github.io/Calculadora-las-70-semanas-de-Daniel/calculadora_daniel_v2.html)
    
> Herramienta interactiva de análisis aritmético-profético de Daniel 9:24–27  
> Desarrollada por **Eugenio F. Martínez Mora** con asistencia de ChatGPT (OpenAI) y Claude (Anthropic)

---

## 📖 Descripción

Esta aplicación web de página única (`calculadora_daniel_v2.html`) permite explorar y comparar los diferentes métodos de cálculo de la famosa profecía de las "70 Semanas" del libro de Daniel (capítulo 9, versículos 24–27).

La herramienta presenta dos enfoques exegéticos enfrentados:

| Método | Descripción |
|--------|-------------|
| **Crítico-Histórico** | Usa años solares reales (365.2422 días) con suma directa. Asociado con la lectura académica macabea. |
| **Teológico-Apologético** | Usa el "año profético" de Robert Anderson (360 días × 483 = 173,880 días), convertidos luego a años solares. |

Ambos métodos aplican la **corrección del año cero histórico** (el año 0 no existe en el calendario juliano/gregoriano prolépctico), y marcan explícitamente el **quiebre textual entre la semana 69 y la 70** según Daniel 9:26.

---

## ✨ Funcionalidades

### 🔢 Cálculos
- Desglose paso a paso de las tres fases: 7 semanas (49 años) + 62 semanas (434 años) + 1 semana (7 años)
- Hito de las **7 semanas** identificado con su evento histórico correspondiente
- Indicador del **intervalo abierto** entre la semana 69 y la 70 (Dan 9:26)
- Corrección automática del año cero al cruzar de a.C. a d.C.

### 📅 Puntos de partida históricos
| Año | Evento | Respaldo textual |
|-----|--------|-----------------|
| 586 a.C. | Destrucción de Jerusalén (Jeremías) | ⚠ No apoyado directamente |
| 538 a.C. | Edicto de Ciro (Esdras 1) | ⚠ Ordena el Templo, no la ciudad |
| 457 a.C. | Artajerjes a Esdras (Esdras 7) | ✓ Debatido académicamente |
| 444 a.C. | Artajerjes a Nehemías (Nehemías 2) | ✦ Mejor respaldo textual |
| **Personalizado** | Cualquier año ingresado manualmente | ✏ Sin análisis predefinido |

### 📆 Año personalizado
Permite ingresar **cualquier año** como punto de partida, con selector de era (a.C. / d.C.). Los cálculos se actualizan en tiempo real.

### 📊 Línea de tiempo visual
- Dos carriles independientes (uno por método)
- Pines con etiquetas alternadas para evitar solapamientos
- Separador visual entre a.C. y d.C.
- Indicador gráfico del intervalo abierto de la semana 70

### 📋 Tabla comparativa
Muestra todos los puntos de partida simultáneamente en una sola tabla, con ambos métodos de cálculo.

### 📚 Notas académicas expandibles
Acordeón con 6 secciones de análisis exegético:
1. ¿Qué son las "70 semanas"? — Estructura del texto
2. Las 7 semanas (49 años): el hito olvidado
3. El intervalo entre la semana 69 y la 70 (Dan 9:26)
4. El "año profético" de Robert Anderson — Crítica
5. La interpretación macabea (crítico-histórica)
6. Posiciones académicas relevantes (Collins, Goldingay, Longman, Hoehner)

### ⬇ Exportar PDF
Genera un PDF de alta resolución con el estado actual de la aplicación.

### 📱 Diseño responsive
Adaptado para PC, tablet y móvil con tres breakpoints:
- `≤ 900px` — Tablet
- `≤ 640px` — Móvil
- `≤ 380px` — Pantallas muy pequeñas

---

## 🚀 Uso

No requiere instalación ni dependencias locales. Es un archivo HTML autocontenido.

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/daniel-70-semanas.git

# Abrir directamente en el navegador
open calculadora_daniel_v2.html
# o simplemente arrastra el archivo a tu navegador favorito
```

También puede alojarse en **GitHub Pages** sin configuración adicional:

1. Ve a `Settings` → `Pages` en tu repositorio
2. Selecciona la rama `main` y la carpeta raíz `/`
3. La aplicación estará disponible en `https://tu-usuario.github.io/daniel-70-semanas/calculadora_daniel_v2.html`

---

## 🛠 Tecnologías

| Tecnología | Uso |
|-----------|-----|
| HTML5 / CSS3 | Estructura y estilos |
| JavaScript (ES6+) | Lógica de cálculo y renderizado |
| [Playfair Display](https://fonts.google.com/specimen/Playfair+Display) | Tipografía de títulos |
| [Lato](https://fonts.google.com/specimen/Lato) | Tipografía de cuerpo |
| [Source Code Pro](https://fonts.google.com/specimen/Source+Code+Pro) | Bloques matemáticos |
| [html2canvas v1.4.1](https://html2canvas.hertzen.com/) | Captura de pantalla para exportación |
| [jsPDF v2.5.1](https://parall.ax/products/jspdf) | Generación de PDF |

> Las fuentes y librerías externas se cargan desde CDN. La aplicación requiere conexión a internet para cargarlas por primera vez.

---

## 📐 Arquitectura del cálculo

### Corrección del año cero

```
función addYearsBC(base, años):
    resultado = base + años
    si (base < 0 Y resultado >= 0):
        resultado += 1  // el año 0 no existe históricamente
    retornar resultado
```

### Método académico (años solares)
```
Fase 1:  inicio  + 49  años = hito 7 semanas
Fase 2:  hito7   + 434 años = fin semana 69
[quiebre textual — Dan 9:26]
Fase 3:  fin69   + 7   años = fin semana 70
```

### Método apologético (año profético de Anderson)
```
69 semanas × 7 años × 360 días = 173,880 días
173,880 ÷ 365.2422            = 476.07 años solares
inicio + 476.07 años           = fin semana 69
[semana 70: intervalo abierto]
```

---

## 🔐 Autoría y firma digital

El código incluye una firma digital en cuatro capas para preservar la autoría:

1. **Comentario hexadecimal** en el `<head>` con el nombre del autor codificado en hex y su hash SHA-256
2. **Propiedad CSS oculta** `--_auth` en `:root` con el nombre en Base64
3. **Objeto `_manifest`** congelado en JavaScript con metadatos de autoría decodificados en tiempo de ejecución
4. **Firma distribuida `_𝛔`** — el nombre partido en 9 fragmentos Base64 que se reconstruyen en memoria

---

## 📚 Bibliografía académica referenciada

- **John J. Collins** — *Daniel* (Hermeneia Commentary Series), Fortress Press
- **John Goldingay** — *Daniel* (Word Biblical Commentary), Thomas Nelson
- **Louis F. Hartman & Alexander A. Di Lella** — *The Book of Daniel* (Anchor Bible)
- **Ernest C. Lucas** — *Daniel* (Apollos Old Testament Commentary)
- **Harold Hoehner** — *Chronological Aspects of the Life of Christ*, Zondervan
- **Robert Anderson** — *The Coming Prince* (1894)
- **Tremper Longman III** — *Daniel* (NIV Application Commentary)
- **Gleason Archer** — *A Survey of Old Testament Introduction*

---

## ⚖ Licencia

Este proyecto es de uso libre para fines educativos, teológicos y de investigación.  
Se agradece mantener los créditos de autoría al distribuir o modificar.

---

## 👤 Autor

**Eugenio F. Martínez Mora**  
Desarrollado con asistencia de **ChatGPT** (OpenAI) y **Claude** (Anthropic)  
Fecha de creación: 22 de febrero de 2026

---

*"Setenta semanas están decretadas sobre tu pueblo y sobre tu santa ciudad..."*  
— Daniel 9:24
