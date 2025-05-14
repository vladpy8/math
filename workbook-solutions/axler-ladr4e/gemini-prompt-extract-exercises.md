# Gemini exercises extraction prompt

This document is a set of imperative instructions as well as guidelines that Gemini must follow to extract definitions, tasks, and exercises from a math workbook.

If provided, Gemini must focus on the content of the specific chapter(s) or section(s) of the workbook, reading only the specified section(s) and ignoring the rest of the workbook.

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

Singular newline notation is allowed inside MathJax blocks to break lines long enough to fit the screen or in certain cases after `\\` if the entire MathJax block is compact enough to be represented in one screen with only a few line breaks.

### 1.2. Compactness. Fewer words, more math

### 1.2.1. Symbols

Use MathJax and generally accepted math symbols instead of plain text words wherever possible. Math symbols might include, but are not limited to:
- `$ \forall $` for "for all"
- `$ \exists $` for "there exists"
- `$ \in $` for "is an element of"
- `$ \subseteq $` for "is a subset of"
- `$ \{ .. \} $` for "set notation"
- `$ : $` for "such that"

#### 1.2.2. Statements

Pursue, reiterate, and achieve the greatest proportion of math symbols to plain text words possible. Ideally, the result is devoid of plain text words.

If some definition, theorem, task, exercise, or generally any statement might be rewritten in a mathematical way, do it. This might include entire statements, comprising multiple sentences, or even paragraphs.

Smaller statements and inline symbols must be built with MathJax inline notation `$...$` in combination with only a few words. For larger statements potentially spanning multiple lines, use MathJax block notation `$$...$$`.

Compress multiple statements into one MathJax block if achievable.

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

### 1.4. Declarative presentation

Use a declarative presentation of theorems, definitions, exercises, statements, plain text sentences, etc. Use imperative presentation only when it is unavoidable.

Omit redundant pieces of content, such as hints, examples, and explanations, if they do not add value to the statement and forbid the extraction in declarative and compact mathematical form.

Such statements as "Prove that ..." or "Show that ..." are not declarative and should be avoided.

Most illustrative examples are:
- Example 1.7.1
- Example 1.7.2
- Example 1.7.3

### 1.5. Spacing and indentation

Use tabs for indentation.

Place MathJax spacing with `\,`, `\ `, and `\quad` between very special math symbols and the rest of the expression if necessary. This might include, but is not limited to:
- `\` for `\exist` or `\exist !`
- `\,` for complex `i`
- `\quad` for `:`

Determine the spacing based on the context of the expression, as well as visual appearance.

Most illustrative examples are:
- Example 1.7.2
- Example 1.7.3

### 1.6. Specifics

1. Whenever a list consists of an unspecified number of items, write it explicitly with the first, second, and last items. For example, `$ x_1, x_2, \dots, x_n $`.

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

```markdown

### Prove that addition of complex numbers is distributive

Suppose that $ \alpha, \beta, \lambda \in \mathbb{C} $. Then $ \lambda (\alpha + \beta) = \lambda \alpha + \lambda \beta $.

... (proof omitted) ...

```

##### Good example

This definition is more compact and declarative. It compresses the property declaration into one MathJax block and omits excessive wording. It also properly employs the newlines style.

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

Present the output as one file with the extracted content in the Markdown format with MathJax expressions. The output must follow the style guidelines in point 1.

### 2.1. Extraction goal

The main focus of the extraction is on the exercises and tasks.

Omit solutions, proofs, and explanations. The goal is to extract the exercises and tasks only.

Leave empty details sections that are designated for solutions and proofs.

Some of the pieces of content might be omitted if they are not relevant to the exercises and tasks, and forbid the extraction in compact and declarative mathematical form.

### 2.2. Output top-level structure

Each piece of the extracted information belongs to a specific chapter or section of the book. Put it under the corresponding heading in the format: `# Chapter [Number]. [Title]. <br>Section [Number]. [Title].`

Definitions come first in the section under the heading `## Definitions`, if present. They are followed by tasks under the heading `## Tasks`, if present. Finally, exercises come last under the heading `## Exercises [Section Number]`.

Inside each of these groups, present the content in the order of appearance in the source material.

### 2.3. Exercises

Exercises are the list of problems, tasks, or questions at the end of the chapter or section. They are usually presented in a numbered list format, in the form of open questions or problems to solve.

The entire exercises section under a level 2 heading must contain one page reference to the beginning of the exercises section in the source text, in the format `Reference page [Number]`. Put it at the beginning of the section, after the heading.

Start each exercise with a heading in the format: `### Exercise [Section].[Number]. [Title]`. The title should be compact, declarative, and descriptive. It is optional and should be present only if the exercise is general enough to have a title.

If an exercise references theorems, examples, or statements that are critical for the solution of the task, then extract the corresponding content together with the exercise.

Each exercise must present the minimum sufficient information to understand and solve it.

### 2.4. Tasks

A task is a broader term, but in terms of the extraction, it is used to refer to exercises that are incorporated into the text of the chapter or section and differ from the exercises at the end of the chapter or section. They are usually what the reader is asked to do in the text and might be presented with phrases such as "Reader should verify that ..." or "Reader can show that ...".

Present tasks with a heading in the format: `### [Title]`. The title should be very short, declarative, and descriptive. Ensure it is as short as possible but still descriptive enough to understand the task. It must be compact and declarative.

For each task, place a page reference to the beginning of the task in the source text. Comply with the format `Reference page [Number]`. It must be at the beginning of the task.

### 2.5. Definitions

Together with exercises and tasks, definitions might also be extracted if they are actively referenced in multiple exercises and tasks and are an essential part of proofs, solutions, and explanations.

Each definition is presented with a heading in the format: `### Definition [Title]`. The title should be very short, descriptive, compact, and declarative.

### 2.6. Avoid tasks duplication

Tasks and exercises must not be duplicated. If a task is already present in the exercises section, or there is complete overlap between the task and an exercise, omit the task.

In case of duplication, put the page reference of the beginning of the task in the source text. Put it in the beginning of the exercise. Comply with the format `Reference page [Number]`.
