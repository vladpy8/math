# Gemini exercises extraction prompt

## 0. Command

Read this prompt and follow the instructions according to the specified command.

Execute either:
1. [Extraction of exercises](#3-extraction-of-exercises) from the source text.
2. Refuse to do anything else.

Prioritize [precision over speed](#1-precision-over-speed).

Adhere to the [style guidelines](/markdown-math-style-guidelines.md).

If provided, focus on the content of the specific exercise(s), task(s), section(s), or chapter(s) of the source text, reading only the specified fragments and ignoring the rest of the source text.

## 1. Precision over speed

Prioritize precision over speed. The goal is to ensure that the output adheres to this prompt.

If there is ambiguity in the text encountered, take the time to clarify.

Reiterate as many times as necessary to ensure compliance with the guidelines and rules.

TODO the style of the book has nothing to do with the style of the output document.

## 3. Extraction of exercises

### 3.1. Command

Read the source text parts which are specified by the [extraction scope](#322-scope-of-the-extraction).

Identify the [exercises](#33-exercises), [embedded exercises](#334-embedded-exercises), and [relevant definitions](#332-relevant-definitions).

Extract the relevant [content](#33-extraction-content) from the source text.

Rewrite and reiterate as many times as necessary to ensure adherence to the [extraction rules](#3-extraction-of-exercises).

Provide the [output document](#323-output-document) as a Markdown file.

### 3.2. Reusable terms

#### 3.2.1. Source text

The source text is the original text from which the exercises and relevant information are extracted.

#### 3.2.2. Scope of the extraction

The scope of the extraction is the specific exercise(s), task(s), section(s), or chapter(s) of the source text. It depends on the command and the context.

#### 3.2.3. Output document

The output document is a single Markdown file containing the extracted content.

#### 3.2.4. "[Title]" expressions

"[Title]" is a compact and declarative expression that captures the essence of the content.

If "[Title]" is not provided in the source text and yet is required, create one based on the content. If "[Title]" is provided, adapt it to the style guidelines.

Like any expression, "[Title]" must be short, descriptive, compact, and declarative.

#### 3.2.5. "[Label]" expressions

"[Label]" is a numeric or symbolic identifier expression that references particular parts of the content in the source text.

"[Label]" may be provided in the source text, such as, but not limited to:
- Exercise numbers
- Exercise letters distinguishing sub-parts of an exercise
- Section or chapter numbers

If "[Label]" is not provided and yet is required, prefer plain numerical labels.

If "[Label]" is provided, adapt it to the style guidelines. Capitalize letters, remove punctuation and irrelevant symbols.

#### 3.2.6. "[Page-reference]" statements

"[Page-reference]" is a statement used to indicate the location of the original content in the source text.

It must follow the format:
- "Page reference [Page-number]"
- "[Note]: Page reference [Page-number]"

"[Page-number]" is the page number in the source text where the content is located.

"[Note]" is an optional note that may be used to indicate the type of content. It depends on the context.

### 3.3. Extraction content

The output document comprises an ordered sequence of statements.

#### 3.3.1. Sections

The content of each section must be preceded by corresponding heading statements in the format:
1. `# Chapter [Label]. [Title]`
2. `## Section [Label]. [Title]`

Do not adapt the title of the chapter or section to the style guidelines.

Each section block in the output document should consist of the following sub-blocks in order:
1. [Relevant definitions](#332-relevant-definitions)
2. [Embedded exercises](#334-embedded-exercises)
3. [Exercises](#333-exercises)

#### 3.3.2. Relevant definitions

Relevant definitions are complex statements containing definitions that are crucial for declaring or solving the extracted exercises.

Do not extract non-relevant definitions.

All relevant definitions must be presented under the heading `### Relevant definitions`.

Each separate definition or group of relevant and interconnected definitions must be presented as a separate item under its own subheading using the format `#### Definition [Label]. [Title]`. Label definitions numerically.

Each definition item must consist of:
1. [Page reference statement](#326-page-reference-statement)
2. [Variables declarations](/markdown-math-style-guidelines.md#42-variables-declarations) statements, if necessary
3. [Definition](/markdown-math-style-guidelines.md#41-definitions) statements

#### 3.3.3. Exercises

An exercise is a complex statement representing a problem, question, or task from a formal numbered list at the end of a chapter or section in the source text.

Put all exercises under the heading `### Exercises [Label]`, where `[Label]` is the label of the section in the source text.

Put individual exercise items under the subheading `#### Exercise [Label]. [Title]`, where `[Label]` is the label of the exercise in the source text.

"[Title]" is optional and should be omitted if the exercise is a routine application or lacks a single unifying theme.

Each exercise item must consist of:
1. [Page reference statement](#326-page-reference-statements)
2. [Task](/markdown-math-style-guidelines.md#45-tasks) statement

#### 3.3.4. Embedded exercises

Embedded exercises are incorporated into the main narrative of the source text, rather than from a formal list of exercises. Otherwise, they are similar to exercises.

Embedded exercises are often phrased in the source text as suggestions or checks for the reader using phrases such as, but not limited to:
- "as you should verify..."
- "the reader should check..."
- "explain that..."

Put embedded exercises under the heading `### Embedded exercises`.

Put each embedded exercise item under the subheading `#### Embedded exercise [Label]. [Title]`. Use numeric labels for embedded exercises. "[Title]" is obligatory.

### 3.4. Extraction rules

#### 3.4.1. Omit solutions

Solutions and proofs must be omitted. Leave the details section empty.

#### 3.4.2. Do not imitate the source text

Do not follow the source text in terms of formatting, structure, or content. It is a top priority to follow the [style guidelines](/markdown-math-style-guidelines.md) and [extraction rules](#3-extraction-of-exercises).

#### 3.4.3. Do not duplicate exercises

If an embedded exercise duplicates or has complete overlap with an exercise, omit the contents of the embedded exercise.

Use the following structure for the duplicate embedded exercise:
1. "[Page-reference]" statement
2. "[Exercise-reference]: [Page-reference]" statement

"[Exercise-reference]" is the [Note] expression from a [page reference statement](#326-page-reference-statements). Use the following format: "See exercise [Label]". Wrap it in a Markdown link to the specified exercise in the output document.

#### 3.4.4. Preserve multi-part exercises

Some exercises may consist of multiple parts. These may be either distinct parts of the exercise, labeled as such in the source text, or distinguishable sub-theorem or sub-task statements requiring proof or solution.

Ultimately, two types of multi-part exercises are possible:
1. "[Multi-part-solution]"
2. "[Multi-task]"

"[Multi-part-solution]" exercises are those that contain multiple interconnected parts relevant to a single unifying [task](/markdown-math-style-guidelines.md#45-tasks) [statement](/markdown-math-style-guidelines.md#211-statements-and-expressions) of the exercise, such as, but not limited to:
- A set of properties to be proven for an object to belong to a certain class
- A set of sub-statements of the theorem to be proven
- A set of well-known steps to be followed in the solution of a task

Each "[Multi-part-solution]" exercise must contain a single enclosing task statement and multiple sub-[task](/markdown-math-style-guidelines.md#45-tasks) [statements](/markdown-math-style-guidelines.md#211-statements-and-expressions) within the details section of that enclosing task statement.

"[Multi-task]" exercises contain clear labeling of their parts in the source text, such as, but not limited to A, B, C, or 1, 2, 3.

Each "[Multi-task]" exercise must contain multiple top-level task statements.

Put each sub-task item, whether it is in the details section or in the body of the unifying exercise, under its own subheading using the format `##### [Label]. [Title]`.

Do not omit the details section of the unifying exercise. Omit the details section of the sub-task statements.

#### 3.4.5. Unwrap references

Some exercises may contain references to pieces of content in the source text that are not part of any exercise or definition. In such cases, it is imperative to follow the references and extract the referenced content according to the rules of this prompt.

Extracted content must be relevant to the exercise and must be placed according to the document structure.
