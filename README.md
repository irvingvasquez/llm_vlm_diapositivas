# LLMs y VLMs

Diapositivas del curso **LLMs & VLMs** (modelos de lenguaje y de visión-lenguaje), impartido en el Instituto Politécnico Nacional (ESCOM / CIDETEC).

El curso recorre cómo se construye un modelo de lenguaje: del panorama de la IA generativa al preprocesamiento del texto, los embeddings y el mecanismo de atención que sostiene la arquitectura Transformer.

| | |
|---|---|
| **Instructor** | Juan Irving Vásquez Gómez |
| **Contacto** | jvasquezg@ipn.mx · [jivg.org](https://jivg.org) |
| **Referencia principal** | Raschka, Sebastian. *Build a Large Language Model (From Scratch)*. Simon and Schuster, 2024. |

---

## Contenido del repositorio

```
llm_vlm_diapositivas/
├── 01_intro_llms/          # Introducción a los LLM
├── 02_preprocesamiento/    # Tokenización, embeddings y codificación posicional
├── 03_attention/           # Mecanismos de atención
├── 04_LLM/                 # Módulo en preparación
└── README.md
```

Cada carpeta de lección guarda la fuente Beamer (`.tex`), las figuras y el PDF compilado.

## Lecciones

Cada fila enlaza al PDF de la presentación.

| # | Tema | Carpeta | PDF |
|---|------|---------|-----|
| 01 | Introducción a los modelos de lenguaje | [`01_intro_llms`](01_intro_llms) | [PDF](01_intro_llms/dlc_intro_llms.pdf) |
| 02 | Preprocesamiento: del texto a los embeddings | [`02_preprocesamiento`](02_preprocesamiento) | [PDF](02_preprocesamiento/dl_preprocesamiento.pdf) |
| 03 | Mecanismos de atención | [`03_attention`](03_attention) | [PDF](03_attention/dl_attention_mechanism.pdf) |

### Qué cubre cada lección

**01. Introducción.** Qué es un LLM, su lugar entre la IA, el aprendizaje profundo y la IA generativa, el entrenamiento en dos etapas (preentrenamiento y ajuste fino), la base Transformer (BERT y GPT), las leyes de escalamiento y el plan del curso: datos, atención, preentrenamiento y ajuste fino.

**02. Preprocesamiento.** Tokenización y Byte Pair Encoding, tokens especiales y tamaño del vocabulario, indexado, embeddings de palabras y de oraciones, el pase hacia adelante de los embeddings de GPT-2, codificación posicional absoluta y la de GPT-2, y la ventana deslizante para predecir el siguiente token.

**03. Atención.** Motivación frente a las redes recurrentes, atención por producto punto escalado, autoatención y atención cruzada, enmascaramiento causal, atención multicabeza y el paso de las fórmulas a la estructura en PyTorch.

---

## Recursos relacionados

| Recurso | Enlace |
|---------|--------|
| Curso previo de redes neuronales | [diapositivas_redes_neuronales](https://github.com/irvingvasquez/diapositivas_redes_neuronales) |
| Curso en línea de redes neuronales | [jivg.org — Introducción a las redes neuronales](https://jivg.org/cursos/introduccion-a-las-redes-neuronales-2/) |

---

## Compilar las diapositivas

Las presentaciones usan [Beamer](https://ctan.org/pkg/beamer) con el tema Metropolis, en formato 16:9.

```bash
cd 02_preprocesamiento
pdflatex dl_preprocesamiento.tex
pdflatex dl_preprocesamiento.tex
```

Los artefactos de compilación (`.aux`, `.log`, `.nav`, `.toc`, `.synctex.gz`, etc.) están en `.gitignore` y no se versionan.
