# Gemini exercises extraction prompt

This document is a set of imperative instructions as well as guidelines that Gemini must follow to extract definitions, tasks, and exercises from a math workbook.

If provided, Gemini must focus on the content of the specific exercise(s), task(s), section(s) or chapter(s) of the workbook, reading only the specified fragments and ignoring the rest of the workbook.

## 0. Precision over speed

Prioritize accuracy and precision over speed. The goal is to ensure that the extracted content is correct, complete, and adheres to the specified format.

If there is ambiguity in the text encountered, take the time to clarify and verify.

Reiterate as many times as necessary to ensure compliance with the guidelines.

## 1. Markdown and MathJax style guidelines

### 1.1. Newlines

Put double newlines after every logically separate piece of content, such as, but not limited to:
- Headings
- A sequence of plain text sentences
- MathJax block expressions `$$...$$`
- MathJax inline expressions `$...$` if they are not part of a sentence
- Inside complicated multiline MathJax blocks with `\\` long enough to not fit the screen if separated by a single newline

Each coherent logical block of text and code must be separated by a double newline. Break lines only at the end of a sentence or at the end of a logical block.

MathJax blocks might be incorporated into sentences, but they must be presented at the end of the sentence and separated by a double newline from the rest of the text.

Singular newline notation is allowed inside MathJax blocks to break lines long enough to fit the screen or in certain cases after `\\` if the entire MathJax block is compact enough to be represented on one screen with only a few line breaks.

### 1.2. Compactness. Fewer words, more math

#### 1.2.1. Symbols

Use MathJax and generally accepted math symbols instead of plain text words wherever possible. Prioritize standard mathematical notation. Math symbols might include, but are not limited to:
- `$ \forall $` for "for all"
- `$ \exists $` for "there exists"
- `$ \in $` for "is an element of"
- `$ \subseteq $` for "is a subset of"
- `$ \{ .. \} $` for "set notation"
- `$ : $` for "such that"

#### 1.2.2. Statements

Pursue, reiterate, and achieve the greatest proportion of math symbols to plain text words possible. Ideally, the core mathematical statement is devoid of unnecessary explanatory prose.

If a definition, theorem, task, exercise, or generally any statement can be rewritten in a more direct mathematical way without loss of meaning or necessary context, do so. This might include entire statements, comprising multiple sentences, or even paragraphs.

Smaller statements and inline symbols must be built with MathJax inline notation `$...$` in combination with minimal surrounding words. For larger statements potentially spanning multiple lines, use MathJax block notation `$$...$$`.

Compress multiple related mathematical statements into one MathJax block if achievable.

Most illustrative examples are:
- Example 1.7.1
- Example 1.7.2
- Example 1.7.3

### 1.3. Details section

Use details sections to hide the proof of theorems, solutions of exercises or tasks, explanations, etc.

```markdown

<details>

<summary>Proof</summary>

...

</details>

```

The content of the details section must adhere to the same style guidelines as the main text.

Details might be nested within other details sections.

Possible summary titles are, but not limited to:
- Proof
- Solution
- Explanation

### 1.4. Declarative presentation

Use a declarative presentation of theorems, definitions, exercises, statements, plain text sentences, etc. Use imperative presentation only when it is unavoidable.

Omit redundant pieces of content, such as introductory phrases, hints, examples within the main text, and explanations if they are not integral to understanding the problem statement of an exercise or the core definition, theorem itself. The focus is on extracting the formal statement.

Statements such as "Prove that ..." or "Show that ..." are not declarative and should generally be rephrased into a direct assertion of the property to be proven. For example, instead of "Prove that $A=B$", state "$$ A=B $$". The proof itself will be hidden in a details section.

Most illustrative examples are:
- Example 1.7.1
- Example 1.7.2
- Example 1.7.3

### 1.5. Spacing and indentation

Use tabs for indentation.

Place MathJax spacing commands such as `\,`, `\ ` and `\quad` judiciously between special math symbols and the rest of the expression if necessary for visual clarity. This might include, but is not limited to:
- `\` (backslash-space) for `\exists` or `\exists !`
- `\,` (thin space) for complex `i` or before differentials like `dx`
- `\quad` (quad space) for separating conditions or logical parts within a single MathJax line.

Determine the spacing based on mathematical typesetting conventions and visual appearance of both source code and rendered output.

Place whitespaces between MathJax symbols for source code readability.

Most illustrative examples are:
- Example 1.7.2
- Example 1.7.3

### 1.6. Specifics

1. Whenever a list consists of an unspecified number of items, write it explicitly with the first, second, and last items, using ellipsis. For example, `$ x_1, x_2, \dots, x_n $`.

2. Never capitalize words after first in a sentence.

### 1.7. Examples

The good examples presented below comply with the style guidelines. Use them as a reference for clarification and derivation of additional implicit guidelines and rules, if necessary.

#### 1.7.1. Example. Definition of complex numbers

##### Good example

This definition is compact and declarative. It leverages math symbols, employs MathJax blocks to represent major interconnected definitions and properties. It follows style guidelines. Yet, it contains all the necessary information, including the components, representation, imaginary unit, addition, and multiplication.

```markdown

### Complex numbers

$ \mathbb{C} $ is the set of complex numbers:

$$ \mathbb{C} = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

$$ i^2 = -1 $$

$ \forall \alpha, \beta \in \mathbb{C} $

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i

\end{aligned}
$$

```

#### 1.7.2. Example. Commutativity of addition of complex numbers

##### Bad example

This statement is too verbose and contains excessive wording that might be rewritten in a more mathematical way. It is not declarative and contains unnecessary explanations. It also does not follow the newlines and spacing styles.

```markdown

### Prove that addition of complex numbers is distributive

Suppose that $\alpha,\beta,\lambda \in \mathbb{C}$. Then $\lambda(\alpha+\beta) = \lambda\alpha +\lambda\beta$.

... (proof omitted) ...

```

##### Good example

This definition is made to follow the style guidelines. It is compact, declarative, and uses MathJax blocks to represent the mathematical statement. It also includes a details section for the proof.

A long line in the first MathJax block is split by single newlines so that the source code fits the screen.

A long line in the second MathJax block is split by double newlines so that the rendered output fits the screen. Alignment is used in order to make it more readable and interconnected across lines.

Whitespaces style adherence ensures readability of the source code.

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

#### 1.7.3. Example. Square root of $ i $

##### Bad example

```markdown

### Find square roots of $ i $

Find distinct square roots of $ i $.

... (solution omitted) ...

```

##### Good example

Imperative command here is shortened and most of the statement is rewritten in a declarative and mathematical way.

Many MathJax block expressions are natural continuation of the preceding sentences, but with double newline separator.

Title is compact and declarative and essentially contains the main statement of the exercise.

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

One complex number equation leads to two real number equations

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

Verifying

$$
\begin{aligned}

\left( \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \right)^2 &= \left( \frac{1}{\sqrt2} \right)^2 + 2 \left( \frac{1}{\sqrt2} \right) \left( \frac{1}{\sqrt2} \, i \right) + \left( \frac{1}{\sqrt2} \, i \right)^2 \\

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

## 2. Extraction of exercises and tasks

### 2.0. Output format

Present output as one file with the extracted content in Markdown format with MathJax expressions. The output must follow the style guidelines in Section 1 of this prompt.

### 2.1. Extraction goal

The main focus of the extraction is on the exercises and tasks.

Omit solutions, proofs, and detailed explanations from the main visible body of the extracted item. The goal is to extract the problem statements or definitions themselves in a clean, declarative, and compact mathematical form.

Leave empty details sections `<details><summary>Proof</summary>\n\n</details>`, which are designated for solutions, proofs, or extended explanations.

Some pieces of textual content might be omitted if they are not relevant to the formal statement of exercises, tasks, or definitions, and if their inclusion would prevent extraction in a compact and declarative mathematical form.

### 2.2. Output top-level structure

Each piece of extracted information should belong to a specific chapter or section of the book. Put it under the corresponding heading in the format: `# Chapter [Number]. [Title]. <br>Section [Number]. [Title].`.

Definitions come first in the section under the heading `## Definitions`, if present. They are followed by tasks under the heading `## Tasks`, if any. Finally, exercises come last under the heading `## Exercises [Section Number]`.

Inside each of these groups, present the content in the order of appearance in the source material.

### 2.3. Exercises

Exercises are typically lists of problems or questions at the end of a chapter or section, usually numbered.

The entire exercises section (e.g., `## Exercises 1A`) must contain one page reference to the page in the source text where this block of exercises begins. Use the format: `Reference page [Number]`. Place it after the section heading.

Start each exercise with a heading in the format: `### Exercise [Section Number]. [Title]`.

1. The `[Title]` should be compact, declarative, and descriptive.
2. A title is optional. Include it if the exercise introduces a named concept or addresses a distinct, general problem type. If it's a routine application or a multi-part question without a single unifying theme, the title may be omitted.
3. If the book provides a clear, concise title for an exercise, adapt it.

If an exercise references specific theorems, examples, or definitions from the text that are essential for understanding the problem statement itself or its immediate context, then extract the corresponding referenced content along with the exercise.

Each exercise must present the minimum sufficient information needed to understand and solve it.

### 2.4. Tasks

A "task" refers to an exercise or problem that is incorporated into the main text of a chapter or section, rather than being part of a formal numbered list at the end. These are often phrased as suggestions or checks for the reader (e.g., "The reader should verify that...", "One can show that...").

Present tasks with a heading in the format: `### [Title]`. The `[Title]` should be very short, descriptive, compact and declarative. It must capture the main statement or property the task is about.

For each task, place a page reference to its location in the source text. Use the format `Reference page [Number]`. This must appear at the beginning of the task.

### 2.5. Definitions

Extract definitions if they are actively referenced in multiple exercises/tasks or are crucial for stating the extracted problems.

Each definition is presented with a heading in the format: `### Definition [Title]`. The `[Title]` should be very short, descriptive, compact, and declarative.

A page reference to where the definition appears in the source text should be included immediately after the title, in the format `Reference page [Number]`.

### 2.6. Avoid tasks duplication

Tasks and exercises must not be duplicated. If a task found in the main text is identical to (or has complete overlap with) an exercise in the formal exercises section, omit the task.

In case of such duplication, if the task's original location in the text provides useful context not present in the exercises section, you may add a page reference to the task's location at the beginning of the corresponding exercise. Use the format: `Reference page [Number] (Task)`.

### 2.7. Examples

The good examples presented below comply with the style guidelines. Use them as a reference for clarification and derivation of additional implicit guidelines and rules, if necessary.

#### 2.7.1. Example. Key section fragments

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

$ F^n $ is set of coordinate vectors over field $ F $.

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

$$
\begin{aligned}

(\alpha + \beta) + \lambda &= ((a_r + b_r) + (a_i + b_i) \, i) + (l_r + l_i \, i) \\

&= ((a_r + b_r) + l_r) + ((a_i + b_i) + l_i) \, i \\

&= (a_r + (b_r + l_r)) + (a_i + (b_i + l_i)) \, i \\

&= \alpha + (\beta + \lambda)

\end{aligned}
$$

</details>

... (omitted) ...

```
