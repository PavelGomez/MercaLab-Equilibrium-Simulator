# Simulador de mercados 2026

Herramienta pedagógica para modelar mercados con funciones lineales de demanda y oferta. Calcula el equilibrio (P\*, Q\*), compara escenarios antes y después de un shock, y estima las elasticidades precio, ingreso y cruzada de la demanda (Epd, Eid, Ecd) y de la oferta (Epo) en cualquier punto válido de la función. Funciona en cualquier navegador, sin instalación ni conexión a internet.

**Curso:** Introducción a la Economía — Universidad Finis Terrae
**Profesor:** Pável Gómez Valera
**Año:** 2026

---

## Contenido

El simulador tiene seis secciones:

| Sección | Descripción |
|---|---|
| **Inicio** | Presentación del modelo y configuración base por defecto |
| **Cómo usar** | Instrucciones paso a paso para estudiantes, ayudantes y docentes |
| **Simulador** | Modela un mercado en un momento dado; calcula equilibrio y elasticidades |
| **Comparador** | Análisis antes/después de un shock; muestra ΔP, ΔQ y variación de elasticidades |
| **Casos guiados** | 8 escenarios económicos reales para aplicar la cadena causal del modelo |
| **Ejemplo resuelto** | Estándar mínimo de explicación esperada en el curso |

---

## Modelo

La demanda efectiva tiene la forma:

```
Qd = A − B·P
```

donde `A = α₀ + α₂·Y + α₃·Ps + α₄·Pc + α₅·Exp` y `B = −α₁`.

La oferta efectiva:

```
Qs = C + D·P
```

donde `C = β₀ + β₂·Pi + β₃·Tec + β₄·N` y `D = β₁`.

El equilibrio se obtiene igualando `Qd = Qs`.

---

## Elasticidades

El simulador calcula cinco elasticidades **puntuales**, evaluadas en cualquier precio P válido (por defecto P\*):

| Elasticidad | Fórmula | Interpretación |
|---|---|---|
| **Epd** | α₁ · P / Qd(P) | Precio propia de la demanda |
| **Eid** | α₂ · Y / Qd(P) | Ingreso (clasifica bien normal, inferior, de lujo) |
| **Ecd (sust.)** | α₃ · Ps / Qd(P) | Cruzada con el precio del sustituto |
| **Ecd (comp.)** | α₄ · Pc / Qd(P) | Cruzada con el precio del complemento |
| **Epo** | β₁ · P / Qs(P) | Precio propia de la oferta |

Cada elasticidad se clasifica automáticamente (elástica, inelástica, unitaria; bien normal, inferior, de lujo; sustitutos, complementos) y se acompaña de una lectura interpretativa.

El **Comparador** muestra además cómo cambian las elasticidades entre el escenario base y el post-shock (columna Δ).

---

## Uso

Descarga el archivo `index.html` y ábrelo con doble clic en cualquier navegador (Chrome, Edge, Safari, Firefox). No requiere instalación, servidor ni conexión a internet.

También disponible en línea: [pavelgomez.github.io/simulador-mercados-2026](https://pavelgomez.github.io/simulador-mercados-2026/)
