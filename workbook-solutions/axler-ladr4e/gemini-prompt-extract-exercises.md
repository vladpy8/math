# Gemini exercises extraction prompt

## 0. Command

Read this prompt carefully and follow the instructions.

Prioritize [precision over speed](#1-precision-over-speed).

Adhere to the [style guidelines](#2-style-guidelines).

Execute [extraction of exercises and tasks](#3-extraction-of-exercises-and-tasks) from the source text.

If provided, focus on the content of the specific exercise(s), task(s), section(s) or chapter(s) of the source text, reading only the specified fragments and ignoring the rest of the source text.

## 1. Precision over speed

Prioritize precision over speed. The goal is to ensure that the output adheres to this prompt.

If there is ambiguity in the text encountered, take the time to clarify.

Reiterate as many times as necessary to ensure compliance with the guidelines and rules.

## 2. Style guidelines

### 2.1. Reusable terms

#### 2.1.1. Statements and expressions

A **statement** refers to a piece of content, such as, but not limited to:
- Markdown heading
- One plain text sentence, or a sequence of such sentences
- One MathJax block expression `$$ ... $$`

MathJax blocks might be incorporated into statements, but they must be presented at the end of the statement.

MathJax inline expressions `$ ... $` might be incorporated into any part of the statement.

An **expression** is a logically and syntactically separate piece of a statement.

Some statements are *explicitly* defined in this prompt to be **complex statements**. They are composed of multiple sub-statements, each of which is considered to be a separate statement.

#### 2.1.2. Words

**Words** or **Wording** refers to plain text prose that is not part of MathJax or Markdown expressions or commands.

#### 2.1.3. Math symbols

**Math symbols** refer to any non-word characters or sequences of characters that are used to represent mathematical notation, primarily with MathJax. This includes, but is not limited to:
- `$ \mathbb{C} $` for complex numbers
- `$ \mathbb{R} $` for real numbers
- `$ \forall $` for "for all"
- `$ \exist $` for "there exists"
- `$ \in $` for "is an element of"
- `$ \subseteq $` for "is a subset of"
- `$ \{ .. \} $` for a set notation
- `$ : $` for "such that"
- `$ \quad $` for quad space
- `$ \ $` for space

### 2.2. Syntax

#### 2.2.1 Newlines

Put double newlines after every statement, except at the end of the document where a single newline should be used.

Put a single newline before a MathJax block if it is part of a statement and appears at the end of it.

If the rendered output of MathJax blocks is too wide to fit the screen, split it into multiple lines using `\\` or similar rendered newline expressions. This might be applied after such symbols as, but not limited to:
- `$ : \\ $`
- `$ , \\ $`
- logical end of expression
- or before `$ \\ = $ `

Special notation might be used, such as `\begin{aligned} .. \end{aligned}` for better readability. Judge based on the context. The most frequent scenario might include long equations where the first and last lines are short and represent the essence of an equation.

If either the source code of a MathJax block is too wide to fit the screen or it already contains `\\` or similar rendered newline expressions, split it into multiple lines using single newlines after special symbols, such as, but not limited to:
- `$$`
- `\\`
- `:`, `: \quad`, `: \`
- `, `, `, \quad`, `, \ `
- `\begin{...}`, `\begin{...} \`
- last line of the MathJax block
- before `$$` if it is part of a statement at the end of it

If the source code of a MathJax block consists of more than 7 lines, replace single newlines with double newlines inside it. Also, replace the newline with a double newline before a MathJax block if it is part of a statement and appears at the end of it.

#### 2.2.2. Spacing and indentation

Use tabs for indentation.

Place spaces inside MathJax inline expressions between `$` and the expression itself.

Place spaces inside MathJax block expressions between `$$` and the expression itself, if newline rules are not applied.

Place spaces between MathJax symbols.

Place rendered MathJax symbols for spacing to improve readability between special math symbols and the rest of the expression. This might include, but is not limited to:
- `$ \exist \ $`
- `$ \forall \, $`
- `$ : \quad $`
- `$ , \quad $`

For very special math terms, such as, but not limited to, the imaginary unit `$ i $`, use `$ \, $` between the unit and the rest of the expression in case of operations involving it.

#### 2.2.3. Dots

Don't put dots after MathJax blocks.

Don't put dots after Markdown headings.

#### 2.2.4. Capitalization

Never capitalize words after the first word in a statement, except for proper nouns or words that are always capitalized, such as, but not limited to:
- People names
- Names of theorems

#### 2.2.5. Details section

Use details sections to hide proofs of theorems, solutions of exercises or tasks, explanations, etc.

```markdown

<details>
<summary>Proof</summary>

... (one or more internal sub statements) ...

</details>

```

Consider a details section as a complex statement. The internals of the details section consist of one or more internal sub-statements.

Possible details summary titles are, but not limited to:
- Proof
- Solution
- Explanation

#### 2.2.6. Ellipsis

Use an ellipsis `...` to indicate that content is omitted.

### 2.3. Compactness and declarative presentation.

#### 2.3.1. Compact symbols

Use math symbols instead of words wherever possible.

#### 2.3.2. Compact statements

Reduce the size and quantity of statements as much as possible.

Merge statements if they are closely related and might be expressed in a single statement. Merge as many statements as possible.

Remove words from statements. Use math symbols and MathJax inline and block expressions instead. Few words are permitted at the beginning of a statement, or in the course of it if they are absolutely necessary.

Consider a MathJax `$ \text{} $` expression as a plain text one.

An ideal statement consists of no words or very few words at the beginning, and a MathJax block expression encompassing multiple interconnected expressions at the end.

#### 2.3.3. Declarative statements and expressions

Avoid imperative statements, expressions, and wording. The "imperative" usually conveys actions, commands, or instructions.

An expression like "[Action] the [Result]" is less preferable than "[Result]". This might include, but is not limited to:
- "[Prove] the [Theorem]" => "[Theorem]"
- "[Show] that [Property] holds" => "[Property]"
- "[Verify] the [Equality]" => "[Equality]"
- "[Explain] the [Result]" => "[Result]"

The actual proof, solution, or explanation is or will be declared in the details section.

However, imperative commands might be unavoidable wherever the final expression is not known yet, must stay hidden in the details section, or is extremely long, spanning multiple statements that are hard to merge. Then, "[Action] the [Result]" might still be rephrased to be as short as possible. This might include, but not limited to:
- "[Find] the solution for [Equation]" => "Solve [Equation]"
- "[Find] the [Variables] when [Expression] is true" => "Solve for [Variables]: [Expression]"
- "[Verify] if the [Property] holds" => "Verify [Property]"

Some imperative commands might look declarative, but still must be avoided. This might include, but not limited to:
- "[Proof] of the [Theorem]" => "[Theorem]"
- "[Verification] of the [Property]" => "[Property]"

### 2.4. Common types of statements

This section describes only the most common types of statements. It is not exhaustive and does not cover all possible cases.

Evolve new types of statements, modify existing ones, and change wording, punctuation, spacing, newlines, and formatting according to the context and these style guidelines.

#### 2.4.1. Definitions

Statements of this type introduce either a new concept or reference well-known ones.

Express references to well-known concepts using the following structures:
- "[Notation] [Short-description]: [Core-definition]"
- "[Notation] [Short-description]"
- "[Short-description]: [Core-definition]"

Express definitions of new concepts using the following structures:
- "Define [Notation] [Short-description]: [Core-definition]"
- "Define [Notation]: [Core-definition]"
- "[Short-description]: [Core-definition]"

"[Notation]" is a symbolic representation of the concept using a MathJax inline expression.

"[Short-description]" is a short plain text expression naming or framing the concept.

"[Core-definition]" is a formal definition of the concept using a MathJax block expression. It might consist of set builder notation, declaring the set of objects along with their properties, representation, and possible operations.

Omit "[Core-definition]" for well-known concepts based on the context. For example, when key properties are not relevant and unlikely to be referenced.

#### 2.4.2. Variables declarations

Statements of this type introduce variables – symbolic representations of mathematical objects of interest. Variables might represent some auxiliary, intermediate, preconditioned, or scope objects.

Declare variables using the following structures:
- "Let [Notation]: [Core-definition]"
- "Let [Core-definition]"
- "Set [Core-definition]"
- "[Core-definition]"

"[Notation]" and "[Core-definition]" are the same as in the [Definitions](#2-4-1-definitions) section, except they are less general and thus more tied to the context.

"[Core-definition]", in the case of variables, might be represented by a MathJax inline expression if it is very short and simple, such as, but not limited to:
- `$ a = value $`
- `$ a, b \in Set $`
- `$ \forall c, d \in Set $`
- `$ \exists e \in Set $`
- `$ U \subseteq V $`

### 2.5. Examples

The good examples comply with the style guidelines. Use them as a reference and for derivation of additional implicit guidelines and rules, if necessary.

#### 2.5.1. Example. Definition of complex numbers

##### Good example

This definition is compact and declarative.

Each statement uses few words at the beginning and a MathJax block expression at the end.

The first MathJax block is the definition of the imaginary unit $ i $.

The second MathJax block is a definition of complex numbers. It uses set builder notation to declare the set of complex numbers and their representation.

The third MathJax block describes the operations of addition and multiplication of complex numbers.

```markdown

### Complex numbers

The imaginary unit $ i $ satisfies:
$$ i^2 = -1 $$

$ \mathbb{C} $ is set of complex numbers:
$$ \mathbb{C} = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

$ \forall \alpha, \beta \in \mathbb{C} $:
$$
\begin{aligned}
\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\
\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i
\end{aligned}
$$

```

#### 2.5.2. Example. Distributivity of multiplication over addition of complex numbers

##### Bad example

This statement is too verbose and contains excessive wording.

It is not declarative and contains unnecessary explanations.

It does not follow the newline and spacing styles.

```markdown

### Prove that addition of complex numbers is distributive

Suppose that $\alpha,\beta,\lambda \in \mathbb{C}$. Then $\lambda(\alpha+\beta) = \lambda\alpha +\lambda\beta$.

... (proof omitted) ...

```

##### Good example

This example is compact, declarative, and uses MathJax blocks to represent the mathematical statement. It also includes a details section for the proof.

A long line in the first MathJax block is split by single newlines so that the source code fits the screen.

A long line in the second MathJax block is split by double newlines so that the rendered output fits the screen. Alignment is used to make it more readable and interconnected across lines.

```markdown

### Distributivity of multiplication over addition of complex numbers

$$
\forall \alpha, \beta, \lambda \in \mathbb{C} \quad
\lambda  (\alpha + \beta) = \lambda \alpha + \lambda \beta
$$

<details>
<summary>Proof</summary>

$$
\begin{aligned}

\lambda  (\alpha + \beta) &= (l_r + l_i \, i)((a_r + b_r) + (a_i + b_i) \, i) \\

&= (l_r(a_r + b_r) - l_i(a_i + b_i)) + (l_r(a_i + b_i) + l_i(a_r + b_r)) \, i \\

&= (l_r a_r - l_i a_i + l_r b_r - l_i b_i) + (l_r a_i + l_i a_r + l_r b_i + l_i b_r) \, i \\

&= (l_r a_r - l_i a_i) + (l_r b_r - l_i b_i) + (l_r a_i + l_i a_r) \, i + (l_r b_i + l_i b_r) \, i \\

&= ((l_r a_r - l_i a_i) + (l_r a_i + l_i a_r) \, i) + ((l_r b_r - l_i b_i) + (l_r b_i + l_i b_r) \, i) \\

&= \lambda \alpha + \lambda \beta

\end{aligned}
$$

</details>

```

#### 2.5.3. Example. Square root of $ i $

##### Bad example

```markdown

### Find square roots of $ i $

Find distinct square roots of $ i $.

... (solution omitted) ...

```

##### Good example

The imperative command here is short, and most of the statement is written in a compact and declarative way.

Many MathJax block expressions are natural continuations of the preceding sentences but are separated by a double newline.

The title is compact and declarative and essentially contains the main statement of the exercise.

```markdown

### Square roots of $ i $

Solve for $ \alpha \in \mathbb{C} $:

$$ \alpha^2 = i $$

<details>

<summary>Solution</summary>

$$
\begin{aligned}
(a_r + a_i \, i)^2 = i \\
a_r^2 - a_i^2 + 2 a_r a_i \, i = i \\
\end{aligned}
$$

One complex number equation leads to two real number equations:
$$
a_r^2 - a_i^2 = 0 \\
2 a_r a_i \, i = i
$$

From the first equation follows
$$
|a_r| = |a_i|
$$

The second one leads to
$$
a_r a_i > 0 \\
2 |a_r| |a_i| = 1
$$

Thus,
$$ |a_r| = |a_i| = \frac{1}{\sqrt2} \\ $$

And finally,
$$ a_r = a_i = \frac{1}{\sqrt2} \quad \text{or} \quad a_r = a_i = - \frac{1}{\sqrt2} $$

The square roots of $ i $ are:
$$
\frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \quad \
\text{or} \quad -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i
$$

Verifying:
$$
\begin{aligned}

\left( \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \right)^2

&= \left( \frac{1}{\sqrt2} \right)^2 + 2 \left( \frac{1}{\sqrt2} \right) \left( \frac{1}{\sqrt2} \, i \right) + \left( \frac{1}{\sqrt2} \, i \right)^2 \\

&= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2} \\

&= i

\end{aligned}
$$

$$
\begin{aligned}

\left( -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i \right)^2 &= \left( -\frac{1}{\sqrt2} \right)^2 + 2 \left( -\frac{1}{\sqrt2} \right) \left( -\frac{1}{\sqrt2} \, i \right) + \left( -\frac{1}{\sqrt2} \, i \right)^2 \\

&= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2} \\

&= i

\end{aligned}
$$

</details>

```



## 3. Extraction and Formatting Guidelines

This section provides specific instructions for extracting and formatting definitions, tasks, and exercises from the source text. All extracted content must rigorously follow these guidelines and the global [Style Guidelines](#2-style-guidelines).

### 3.1. General Principles

The primary **Extraction Goal** is to capture exercises, tasks, and definitions that are essential for understanding or solving these problems. Problem statements and definitions should be presented in a clean, declarative, and mathematically compact form. To achieve this, verbose explanations or extended derivations present in the source should generally be omitted from the main visible body of the extracted items, unless they are integral to the problem statement itself. Solutions, proofs, and detailed explanations associated with an item must be placed within "details" sections, as specified in Section 3.3.5. Textual content from the source may be omitted if it is not directly relevant to the formal statement of an exercise, task, or definition, or if its inclusion would impede a compact and declarative presentation.

Regarding **Adherence to Prompt Style**, this document's guidelines, including those in [Section 2](#2-style-guidelines), take absolute precedence over the formatting, structure, or wording of the source text.

### 3.2. Reusable Components and Statement Definitions

The following components and specific **complex statement** types are integral to the extraction process.

#### 3.2.1. [Title] Component

A **`[Title]`** is a short, declarative, and descriptive phrase that captures the essence of the item (exercise, task, definition, or sub-part). It must contain no unnecessary wording.
-   If the source text provides a clear and concise title (e.g., for a named theorem or a specifically titled exercise), adapt it to meet these style guidelines.
-   If no title is provided, create one based on the item's content.
-   A `[Title]` is optional for Exercises and multi-part items under specific conditions detailed in Sections 3.2.5 and 3.3.3.

#### 3.2.2. Page Reference Statement

A **Page Reference Statement** is a specific type of statement used to indicate the location of the original content in the source text.
It must use one of the following formats:
-   `Reference page [Number]`
-   `Reference page [Number] (Task)` (This format is used specifically for exercises that duplicate an in-text task, as described in Section 3.3.4).
Replace `[Number]` with the corresponding page number from the source text. This statement is considered a separate statement and must be followed by a double newline. Its placement is specified for each content type.

#### 3.2.3. Definition Statement

A **Definition Statement** is a **complex statement** that introduces a mathematical definition.
Definitions should be extracted if they are actively referenced in multiple exercises or tasks within the current section, or if they are crucial for understanding or stating the extracted problems.
The content and order for a Definition Statement are:
1.  A heading of the format `### Definition [Title]`. The `[Title]` should be derived from the source's named definition (e.g., if the source states "Definition 1.1 Complex Numbers", the title could be 'Complex Numbers'). If the source provides a numbered definition without a descriptive name, use the concept being defined as the `[Title]`.
2.  A Page Reference Statement, placed immediately after the heading.
3.  The definition's core content. This core content is composed of one or more statements as defined in [Section 2.1.1](#2-1-1-statements-and-expressions), structured according to the guidelines in [Section 2.4.1](#2-4-1-definitions), and should be extracted from the source.

#### 3.2.4. Task Statement

A **Task Statement** is a **complex statement** representing an exercise, problem, or specific instruction (such as 'prove that P', 'verify that X', 'show that Y', 'explain why Z', or implicit directives like 'as you should verify...' or 'the reader can/should check/demonstrate...') found within the main narrative of the source text, rather than from a formal list of exercises.
The content and order for a Task Statement are:
1.  A heading of the format `### [Title]`. The `[Title]` must be very short, descriptive, compact, and declarative, typically capturing the main mathematical property or assertion.
2.  A Page Reference Statement, placed immediately after the heading.
3.  The task's core problem description. This description consists of one or more statements (as defined in [Section 2.1.1](#2-1-1-statements-and-expressions)) rephrased from the source into a declarative and compact mathematical form.
4.  A "details" section containing the extracted proof, solution, or explanation, as specified in Section 3.3.5.

For handling multi-part tasks, refer to Section 3.3.3.

#### 3.2.5. Exercise Statement

An **Exercise Statement** is a **complex statement** representing a problem or question, typically from a formal numbered list at the end of a chapter or section in the source text.
The content and order for an Exercise Statement are:
1.  A heading of the format `### Exercise [Section Number].[Optional Title]`. `[Section Number]` refers to its designation in the source (e.g., 1A, 2.3). The `[Optional Title]` part (including the preceding period) should be omitted if the exercise is a routine application or lacks a single unifying theme. If omitted, the format is `### Exercise [Section Number]`.
2.  A Page Reference Statement (only if the exercise duplicates a task, see Section 3.3.4).
3.  The exercise's core problem description. This description consists of one or more statements (as defined in [Section 2.1.1](#2-1-1-statements-and-expressions)) presenting the minimum sufficient information needed to understand and attempt the problem.
4.  A "details" section containing the extracted proof or solution, as specified in Section 3.3.5.
If an exercise critically references specific theorems, examples, or definitions, ensure this referenced content is extracted (as a Definition Statement, etc.) and placed appropriately, typically before the exercise itself or within the section's "Definitions" block if broadly applicable. For handling multi-part exercises, refer to Section 3.3.3.

### 3.3. Output Structure and Content Application

#### 3.3.1. Top-Level Document Structure

All extracted content must be organized into a single Markdown file.
Individual pieces of information must be grouped by their chapter and section in the source text, using a main heading of the format:
`# Chapter [Number]. [Title]. <br>Section [Number]. [Title].`
Within each such section, the content must be ordered under these specific second-level headings:
1.  `## Definitions` (containing all Definition Statements for that section, if any).
2.  `## Tasks` (containing all Task Statements for that section, if any).
3.  `## Exercises [Section Number]` (e.g., `## Exercises 1A`, containing all Exercise Statements for that specific source exercise section).
Individual items within these blocks (Definitions, Tasks, Exercises) must appear in the same order as they do in the source material.

#### 3.3.2. Specifics for Exercises Sections

The collection of all Exercise Statements from a particular numbered exercise section in the source must be grouped under a heading of the format `## Exercises [Section Number]`. Immediately following this heading, a Page Reference Statement must be included to indicate the page in the source text where this block of exercises begins.

#### 3.3.3. Handling Multi-Part Items

If a Task Statement or Exercise Statement consists of multiple distinct parts, each part must be presented as a separate item under its own subheading using the format `#### [Label]. [Optional Title]`.
-   **`[Label]`**: If the source provides labels (e.g., A, B, or 1, 2), use them. Letter labels must be capitalized and consist only of the letter itself. If no labels are provided in the source, use numeric enumeration (1, 2, ...) in order of appearance.
-   **`[Optional Title]`**: A title for a sub-part is optional and should be omitted if the part is a routine application or does not have a clear, unifying theme distinct from other parts. If omitted, the format is `#### [Label]`.
Each sub-part is a complete statement and must be followed by its own "details" section containing the extracted proof/solution (see Section 3.3.5). A task or exercise should be divided into parts if it contains clearly identifiable sub-tasks or distinct questions, such as distinguishable properties or statements to be proven, even if not explicitly labeled in the source. Each sub-part must comply with all style guidelines.

#### 3.3.4. Avoiding Duplication (Tasks vs. Exercises)

No task or exercise should be duplicated. If a task found in the main text is identical to, or has complete overlap with, an exercise in a formal exercise list, then the task must be omitted from extraction. In this case, a Page Reference Statement of the format `Reference page [Number] (Task)` must be placed at the beginning of the corresponding Exercise Statement (immediately after its `###` heading), where `[Number]` is the page where the duplicated task appeared.

#### 3.3.5. Solutions, Proofs, and Explanations (Details Sections)

All solutions, proofs, or detailed explanations associated with an extracted item must be placed *inside* a "details" section, as described in [Section 2.2.5](#2-2-5-details-section). The content within the "details" section must itself adhere to all [Style Guidelines](#2-style-guidelines) from Section 2, including formatting of paragraphs, MathJax, newlines, etc.
The standard summary titles are "Proof", "Solution", or "Explanation". For example: `<details><summary>Proof</summary> ...extracted proof content... </details>`.
The "details" section as a whole is a **complex statement** and should be followed by a double newline, unless it is the last statement in the document.

### 3.4. Self-Correction and Final Review

Before finalizing output, rigorously review all extracted content. Verify precision in mathematical transcription; strict adherence to all [Style Guidelines](#2-style-guidelines); and correct application of all structural and formatting rules detailed in this Section 3, including page references, handling of multi-part items, and placement of solutions/proofs within "details" sections. Reiterate this review and correction process as needed to ensure full compliance with this prompt, prioritizing [precision over speed](#1-precision-over-speed).







## 3. Extraction of exercises and tasks

### 3.1. Reusable terms

#### 3.1.1. Source text

The source text is the original text from which the exercises, tasks, and definitions are extracted.

##### 3.1.1. Task

...

### 3.1. Output format

Present the output as one file containing the extracted content in Markdown format with MathJax expressions. The output must follow the style guidelines in Section 2 of this prompt.

### 3.2. Extraction goal

The main focus of the extraction is on the exercises and tasks.

Omit solutions, proofs, and detailed explanations from the main visible body of the extracted item. The goal is to extract the problem statements or definitions themselves in a clean, declarative, and compact mathematical form.

Some pieces of textual content might be omitted if they are not relevant to the formal statement of exercises, tasks, or definitions, and if their inclusion would prevent extraction in a compact and declarative mathematical form.




#### 2.2.1. `[Title]`

Title of the exercise, task, subtask, or definition.

The title must be compact, declarative, and descriptive. It should be a short phrase that captures the essence of the exercise or task with no unnecessary wording.

If a title is provided by the source text, adapt it to the style guidelines. If no title is provided, create one based on the content of the exercise or task.

### 3.2. Output top-level structure

Each piece of extracted information should belong to a specific chapter or section of the book. Put it under the corresponding heading in the format: `# Chapter [Number]. [Title]. <br>Section [Number]. [Title].`.

Definitions come first in the section under the heading `## Definitions`, if present. They are followed by tasks under the heading `## Tasks`, if any. Finally, exercises come last under the heading `## Exercises [Section Number]`.

Inside each of these groups, present the content in the order of appearance in the source material.

### 3.3. Exercises

Exercises are typically lists of problems or questions at the end of a chapter or section, usually numbered.

The entire exercises section (e.g., `## Exercises 1A`) must contain a page reference to the page in the source text where this block of exercises begins. Use the format: `Reference page [Number]`, where `[Number]` is the corresponding page number in the source text. Place it after the section heading.

Start each exercise with a heading in the format: `### Exercise [Section Number]. [Title]`.

1. The `[Title]` should be compact, declarative, and descriptive.
2. A title is optional. Include it if the exercise introduces a named concept or addresses a distinct, general problem type. If it's a routine application or a multi-part question without a single unifying theme, the title may be omitted.
3. If the book provides a clear, concise title for an exercise, adapt it.

If an exercise references specific theorems, examples, or definitions from the text that are essential for understanding the problem statement itself or its immediate context, then extract the corresponding referenced content along with the exercise.

Each exercise must present the minimum sufficient information needed to understand and solve it.

### 3.4. Tasks

A "task" refers to an exercise or problem that is incorporated into the main text of a chapter or section, rather than being part of a formal numbered list at the end. These are often phrased as suggestions or checks for the reader (e.g., "The reader should verify that...", "One can show that...").

Present tasks with a heading in the format: `### [Title]`. The `[Title]` should be very short, descriptive, compact, and declarative. It must capture the main statement or property the task is about.

For each task, place a page reference to its location in the source text. Use the format `Reference page [Number]`. This must appear at the beginning of the task.

### 3.5. Definitions

Extract definitions if they are actively referenced in multiple exercises/tasks or are crucial for stating the extracted problems.

Each definition is presented with a heading in the format: `### Definition [Title]`. The `[Title]` should be very short, descriptive, compact, and declarative.

A page reference to where the definition appears in the source text should be included immediately after the title, in the format `Reference page [Number]`, where `[Number]` is the corresponding page number in the source text.

### 3.6. Avoid task duplication

Tasks and exercises must not be duplicated.

If a task found in the main text is identical to (or has complete overlap with) an exercise in the formal exercises section, omit the task.

In the case of such duplication, add a page reference to the task's location at the beginning of the corresponding exercise. Use the format: `Reference page [Number] (Task)`, where `[Number]` is the corresponding page number in the source text.

### 3.7. Multi-part tasks and exercises

If a task or exercise consists of multiple parts, each part must be presented as a separate item under its own subheading.

Use original labels, either letters (e.g., A, B) or numbers (e.g., 1, 2), if they are provided in the source text. In this case, use the format: `#### [Label]. [Title]`, where:
1. `[Label]` is the label of the part, capitalized
2. `[Title]` is a short, descriptive, compact, and declarative title. It must be omitted if the part is a routine application or a multi-part question without a single unifying theme.

If `[Label]` is a letter, ensure it is capitalized and use only the letter itself, without any additional symbols or punctuation. For example, `#### A. [Title]`.

If no labels are provided, use numeric enumeration in order of their appearance. Then apply the same format: `#### [Number]. [Title]`, as described above.

In the absence of explicit labels, tasks should be divided into parts if they contain clearly identifiable subtasks or questions. These could be distinguishable properties or statements to be proven.

For each subtask, comply with the same rules and guidelines as for the main task or exercise. This includes the use of page references, titles, and the overall structure.

For nested proofs or solutions, use the same details section format as described in Section 2.2.5. The content of the details section must adhere to the same style guidelines as the main text.

See Example 3.10.2 for a good illustration of a multi-part exercise.

### 3.8 No solutions

Do not include solutions, proofs, or detailed explanations. Leave empty details sections `<details><summary>Proof</summary>\n\n</details>`, which are designated for solutions, proofs, or extended explanations.

### 3.9. Do not follow the source

Do not follow the source text in terms of formatting, structure, or content. It is a top priority to follow the style guidelines and rules outlined in this document.

### 3.10. Examples

The good examples presented below comply with the style guidelines. Use them as a reference for clarification and derivation of additional implicit guidelines and rules, if necessary.

#### 3.10.1. Example. Key section fragments

##### Good example

The key fragments presented here comply with the style guidelines. They are compact, declarative, and use MathJax blocks to represent the key mathematical statements.

```markdown

# Chapter 1. Vector spaces. <br>Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $.

## Definitions

### Complex numbers

... (omitted) ...

### Coordinate vectors $ F^n $

Reference page 6

Let $ F $ be a field of numbers.

$ F^n $ is set of coordinate vectors over field $ F $:
$$ F^n = \{ x: \quad \exist! \ x_1, x_2, \ldots, x_n \in F, \quad x = (x_1, x_2, \ldots, x_n) \} $$

$ \forall x, y \in F^n $ and $ \forall \lambda \in F $

$$
\begin{aligned}

x + y &= (x_1 + y_1, x_2 + y_2, \ldots, x_n + y_n) \\

\lambda x &= (\lambda x_1, \lambda x_2, \ldots, \lambda x_n)

\end{aligned}
$$

## Exercises 1A

Reference page 10

... (omitted) ...

### Exercise 1A.2. Associativity of addition of complex numbers

Reference page 3 (Task)

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $

$$ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) $$

<details>

<summary>Proof</summary>

</details>

... (omitted) ...

```

#### 3.10.2. Example. Multi-part exercise

##### Bad example

It doesn't contain a double newline after the heading.

`Reference page 14 (Task)` is incorrect here, since there are no duplicating tasks on page 14 of the source text.

This statement is very shallow in terms of mathematical content. It is not declarative and contains unnecessary explanations. It also does not follow the newline and spacing styles.

In spite of the fact that there are clear set-in-stone properties to be proven, the statement is not split into parts.

```markdown

### Exercise 1B.7. $ V^S $ is a vector space
Reference page 14 (Task)

Let $ S $ be a nonempty set. Let $ V^S $ denote the set of functions from S to V.
Define a natural addition and scalar multiplication on $ V^S $.
$ V^S $ is a vector space with these definitions.

<details>

<summary>Proof</summary>

</details>

```

##### Good example

This statement is closer to the style guidelines.

Since statement contains clear properties, each of them is assigned a separate block with a title and empty details section.

```markdown

### Exercise 1B.7. $ V^S $ is a vector space

Let $ S $ be an arbitrary nonempty set.

Let $ V $ be a vector space over $ F $.

Let $ V^S $ be a set of functions $ { S \to V } $.

Define addition on $ V^S $:

$$ \forall f, g \in V^S, \quad \forall x \in S, \quad (f + g)(x) = f(x) + g(x) $$

Define scalar multiplication on $ V^S $:

$$
\forall \lambda \in F, \quad
\forall f \in V^S, \quad
\forall x \in S, \quad (\lambda f)(x) = \lambda f(x)
$$

The $ V^S $ is a vector space over $ F $

<details>

<summary>Proof</summary>

#### 1. Commutativity of addition

... (omitted) ...

<details>

<summary>Proof</summary>

... (omitted) ...

</details>

#### 2. Associativity of addition

... (omitted) ...

<details>

<summary>Proof</summary>

... (omitted) ...

</details>

... (omitted) ...

#### 7. Distributivity of addition over scalar multiplication

... (omitted) ...

<details>

<summary>Proof</summary>

... (omitted) ...

</details>

</details>

```
