# The Career Spark

🇬🇧 [English](README.md) | 🇫🇷 [Français](README.fr.md)

Un skill de IA para la creación de currículums y cartas de presentación, mediante extracción estructurada, construcción narrativa y redacción calibrada. La chispa ya está en la carrera del candidato. Este skill la encuentra y la hace visible.

## Qué hace

La mayoría de los currículums infravaloran al candidato. Este skill cierra esa brecha con honestidad.

Toma el CV existente, el historial profesional y las evidencias disponibles, extrae habilidades ocultas, construye una narrativa estratégica de carrera y produce materiales de candidatura que son completamente honestos y máximamente convincentes. Se desarrolló a partir de un proyecto real de reformulación de CV donde 44 habilidades declaradas se convirtieron en 134 tras la extracción e inferencia, con categorías enteras completamente ausentes del CV original.

**El objetivo:** Ayudar al candidato a conseguir entrevistas para puestos donde realmente prosperará, mediante materiales que lo representen fielmente en su mejor versión.

## Cómo funciona

Siete fases, cada una construyendo sobre la anterior:

| Fase | Propósito | Entregable |
|------|-----------|------------|
| 1. Extraer | Encontrar las habilidades reales | Inventario de habilidades con brechas identificadas |
| 2. Narrar | Construir la columna vertebral estratégica | Documento narrativo de carrera |
| 3. Redactar | Crear el currículum | CV en formato(s) objetivo(s) |
| 4. Orientar | Explorar el mercado, asociar puestos, optimizar para ATS | Panorama de puestos, datos salariales, CV optimizado ATS |
| 5. Cubrir | Redactar argumentos dirigidos | Cartas de presentación por puesto |
| 6. Evaluar | Prueba de estrés desde la perspectiva del reclutador | Informe de vulnerabilidades y plan de preparación |
| 7. Entregar | Hacer llegar los materiales a la persona correcta (opcional) | Estrategia de distribución, plan de contacto |

Las correcciones del candidato impulsan el proceso. Cada corrección en el proyecto original hizo el resultado más honesto y más convincente a la vez. El skill integra puntos de control en cada fase.

El proceso soporta trabajo multi-sesión con un mecanismo estructurado de transferencia. Cuando una sesión se extiende, la IA produce un documento de transferencia detallado y empaqueta todos los archivos para que la siguiente sesión retome exactamente donde se dejó.

## Principios clave

- **Extracción antes de redacción.** Nunca escribir un CV desde cero. Extraer habilidades, inferir las que faltan, luego construir.
- **Narrativa antes de formato.** Sin columna vertebral estratégica, el CV es solo una lista de empleos.
- **Altitud exacta.** Ni infravalorar ni sobrevalorar. El objetivo es el encuadre que es completamente honesto y máximamente convincente.
- **Útil significa que el candidato es contratado.** No "el candidato está contento con el documento." La aprobación no es el servicio. El servicio es que el candidato sea contratado para un puesto donde prospere.
- **Calidez y honestidad no compiten.** Los comentarios se entregan con cuidado, no se retienen para evitar fricción. El candidato debe sentir que la IA está de su lado, incluso cuando está en desacuerdo.
- **Deber de vigilancia.** El CV lleva el nombre del candidato. La IA verifica activamente riesgos legales, profesionales y reputacionales, incluidas consecuencias que el candidato no ha anticipado.
- **El candidato siempre tiene razón sobre su propia experiencia.** La IA le ayuda a formularla en el lenguaje del mercado laboral.
- **Generar opciones, no conclusiones.** El rol de la IA es generativo. El rol del candidato es editorial. El candidato debe elegir, no simplemente aceptar.

## Estructura del skill

```
career-spark/
├── SKILL.md                              Flujo de trabajo principal (punto de entrada)
└── references/
    ├── principles.md                     Principios, redefinición de utilidad
    ├── calibration-guide.md              Calibración infravaloración/sobrevaloración
    ├── overclaiming-guide.md             Psicología de la inflación y desescalada
    ├── narrative-archetypes.md           12 arquetipos narrativos de carrera
    ├── evidence-without-portfolio.md     Encontrar evidencia sin portafolio
    ├── cover-letter-guide.md             Marco para cartas de presentación dirigidas
    ├── application-intelligence.md       Cartografía, estrategia de distribución
    ├── candidate-psychology.md           Estados emocionales, resistencias, conflictos de imagen
    └── cultural-norms.md                 Convenciones de CV por país/región
```

El SKILL.md es el punto de entrada. Los archivos de referencia se cargan bajo demanda según la fase y la situación del candidato. El paquete `.skill` contiene solo estos 10 archivos. README y LICENSE son para el repositorio, no para la IA.

## Para quién es

- **Profesionales experimentados** en transición o reposicionamiento de carrera
- **Candidatos en mitad de carrera** que infravaloran sus habilidades
- **Cualquier persona que busque puestos específicos** que necesite materiales personalizados, no un simple pulido genérico
- **Candidatos en inicio de carrera** que necesitan encuadrar experiencia limitada
- **Candidatos internacionales** que apuntan a mercados con diferentes convenciones de CV
- **Candidatos con un puesto soñado** que quieren maximizar sus oportunidades mediante investigación organizacional y distribución estratégica

## Lo que este skill NO hace

Este skill produce currículums, cartas de presentación, la narrativa estratégica que los sustenta y (opcionalmente) una estrategia de distribución. No cubre preparación de entrevistas, negociación salarial ni estrategia de LinkedIn. Sin embargo, sus resultados (narrativa de carrera, inventario de habilidades, investigación organizacional e historias de entrevista recopiladas) están diseñados como inputs naturales para esas actividades.

## Instalación

### Como Skill de Claude

Descargue el archivo `.skill` desde la página de [Releases](../../releases) e instálelo en su entorno Claude.

### Gemini

Use el [Career Spark Gem](https://gemini.google.com/gem/1G_9r7u-X_TKPIX5MsdDz-WNJK3EU3n0_?usp=sharing) directamente. Para mejores resultados, seleccione el modelo con la mayor capacidad de razonamiento. Pro es recomendado. El modo Thinking es una buena alternativa. Fast funcionará pero puede perder matices en la calibración y adaptación psicológica.

### ChatGPT

Use el [Career Spark CustomGPT](https://chatgpt.com/g/g-69d26d47523881919acd487ef609384a-the-career-spark). Seleccione el mejor modelo disponible. Nota: el CustomGPT no puede acceder a sus memorias ni a su historial de conversación. Si necesita que el skill utilice conversaciones previas o contexto personal, descargue el archivo `.skill` desde la página de [Releases](../../releases) y deposítelo directamente en una conversación.

### Otros proveedores de IA

El archivo `.skill` es un archivo zip estándar. Descárguelo desde la página de [Releases](../../releases), renómbrelo de `career-spark.skill` a `career-spark.zip`, súbalo a su plataforma y pida al modelo que use el skill contenido en el archivo zip. El `SKILL.md` es el punto de entrada; los archivos de referencia en `references/` se cargan según necesidad. Use el modelo más potente disponible en su plataforma.

### Manual

Clone o descargue este repositorio. Apunte su herramienta de IA al archivo `SKILL.md` como punto de entrada.

## Origen

Este skill se desarrolló a partir de un proyecto real de reformulación de CV (marzo-abril 2026) entre [Ivan "HiP" Phan](https://github.com/hip1) y Claude. El proceso de cuatro sesiones que produjo el CV original fue documentado, luego generalizado y extendido en una sesión dedicada de creación de skill para convertirlo en una herramienta aplicable a cualquier candidato en cualquier sector.

Cada principio fue descubierto en la práctica y refinado mediante las correcciones del candidato. Las correcciones del candidato fueron el aporte más valioso del proyecto original. Un proceso que no integra bucles de corrección producirá currículums pulidos pero incorrectos. Esa observación es el fundamento de todo el skill.

## Licencia

Licencia MIT. Ver [LICENSE](LICENSE) para los detalles.
