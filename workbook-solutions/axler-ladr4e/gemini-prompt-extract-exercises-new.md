# Gemini exercises extraction prompt

This document is set of imperative instruction Gemini must follow to extract definitions, tasks and exercises from math workbook. The instructions are designed to ensure the transcription is accurate, complete, and adheres to a specific format.

If provided, Gemini must focus on the content of the specific chapter or sections of the workbook

## 0. Precision over speed

Gemini must prioritize accuracy and precision over speed. The goal is to ensure that the extracted content is correct, complete, and adheres to the specified format. If Gemini encounters any uncertainty or ambiguity in the text, it should take the time to clarify, verify or reiterate before proceeding.

It is especially important in regards to points 1.2 and 1.4 of the style guide.

## 1. Markdown and MathJax style guide

### 1.0. Examples

#### 1.0.1. Example

```markdown

### Complex numbers

$ \mathbb{C} $ is set of complex numbers

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

#### 1.0.2. Example

```markdown

### Commutativity of addition of complex numbers

$ \forall \alpha, \beta \in \mathbb{C} $

$$ \alpha + \beta = \beta + \alpha $$

<details>

<summary>Proof</summary>

$$
\begin{aligned}

\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\

&= (b_r + a_r) + (b_i + a_i) \, i \\

&= \beta + \alpha

\end{aligned}
$$

</details>

```

#### 1.0.3. Example

This is bad example of a statement:

```markdown

Suppose that $ b \in \R $. Show that set of continuous real-valued functions $ f $ on the interval $ [0,1] $ such that $ \int_0^1 f = b $ is a subspace of $ R^{[0,1]} $ if and only if $ b = 0 $.

```

It is not declarative. It doesn't use MathJax notation. It is not compact. It doesn't use newlines style. It doesn't use details section.

It must be rewritten as:

```markdown

Let $ b \in \R $.

Let $ U \subseteq \R^{[0,1]} $:

$$ U = \{ f \in \R^{[0,1]} : f \ \text{is continuous on} \ (0,1) \ \text{and} \ \int_0^1 f = b \} $$

Then

$$ U \, \text{is a subspace of} \, \R^{[0,1]} \iff b = 0 $$

<details>

<summary>Proof</summary>

...

</details>

```

(As an important note, $ U \subseteq \R^{[0,1]} $ means that $ U $ is set of real-valued functions)

### 1.1. Newlines

Put double newlines after every logically separate piece of content, such as, but not limited to:
- Headings
- Sequence of plain text sentences
- MathJax block expressions `$$...$$`
- MathJax inline expressions `$...$` if they are not part of a sentence
- Inside complicated multiline MathJax blocks with `\\`

Each coherent logical block of text and code must be separated by a double newline. Break lines only at the end of a sentence or at the end of a logical block.

Singular newline notation is allowed inside display MathJax blocks to break lines long enough to fit the screen.

### 1.2. Less words, more math (LWMM)

### 1.2.1. Symbols

Use MathJax and generally accepted math symbols instead of plain text words wherever possible. Math symbols might include, but are not limited to:
- $ \forall $ for "for all"
- $ \exists $ for "there exists"
- $ \in $ for "is an element of"
- $ \subseteq $ for "is a subset of"
- $ \{ .. \} $ for "set notation"
- $ : $ for "such that"

#### 1.2.2. Statements

Pursue, reiterate and achieve the greatest proportion of math symbols to plain text words possible. Ideally if the result is devoid of plain text words.

If some definition, theorem, task, exercise or generally any statement might be rewritten in a mathematical way, do it. This might include entire statements, comprising of multiple sentences, or even paragraphs.

Smaller statements and inline symbols must be built with inline MathJax `$...$` notation in combination with only few words. For larger statements potentially spanning multiple lines, use display MathJax `$$...$$` notation.

Compress multiple statements into one display MathJax block if achievable.

For example, the statement is considered to be a good candidate for rewriting:

```markdown

The sum of $ V_1, V_2, \dots, V_m $, denoted by $ V_1 + V_2 + \dots + V_m $, is the set of all possible sums of elements of $ V_1, V_2, \dots, V_m $.

```

It might be rewritten as:

```markdown

Define the sum of $ V_1, V_2, \dots, V_m $:

$$

V_1 + V_2 + \dots + V_m = \{
	v_1 + v_2 + \dots + v_m :
	\quad v_1 \in V_1, v_2 \in V_2, \dots, v_m \in V_m
\}

$$

```

Which leverages use of set building notation and the colon $ : $ symbol. Moreover, it is more compact and less verbose and properly employs newlines style.

This example is a good candidate for rewriting as well:

```markdown

Let $ \alpha = \frac{-1 + \sqrt{3}i}{2} $.
Then $ \alpha $ is a cube root of $ 1 $ (meaning that its cube equals $ 1 $).

```

It might be rewritten as:

```markdown

Let

$$ \alpha = \frac{-1 + \sqrt{3} \, i}{2} $$

Then

$$ \alpha ^3 = 1 $$

```

### 1.3. Details section

Use details sections to hide the proof of theorems, solutions of exercises or tasks, explanations, etc.

```markdown

<details>

<summary>Proof</summary>

...

</details>

```

### 1.4. Declarative presentation

Use declarative presentation of theorems, definitions, exercises, etc. Use imperative presentation only when it is unavoidable.

Such statements as "Prove that ..." or "Show that ..." are not declarative and should be avoided. For example, the statement is good candidate for rewriting:

```markdown

Prove that for each complex number there exists a multiplicative inverse.

```

It might be rewritten as:

```markdown

$$ \forall \alpha \in \mathbb{C}, \quad \exist \  \beta \in \mathbb{C} : \quad \alpha \, \beta = 1 $$

<details>

<summary>Proof</summary>

...

</details>

```

This example is a good candidate for rewriting, however it is impossible to rewrite it in a declarative way:

```markdown

Find two distinct square roots of $ i $.

```

The following statement might be used instead:

```markdown

Solve for $ \alpha \in \mathbb{C} $

$$ \alpha^2 = i $$

```

### 1.5. Specifics

1. Whenever a lists consists of unspecified number of items write it explicitly with first, second and last items. For example $ x_1, x_2, \dots, x_n $

## 2. Extraction of exercises and tasks

### 2.0. Output format

Output must be presented as one or multiple files with the extracted content in the markdown format with MathJax expressions. The output must follow the style guide above in point 1.

### 2.1. Extraction goal

The main focus of the extraction is on the exercises and tasks.

Exercises are the end of the chapter or section list of problems, tasks or questions. They are usually presented in a numbered list format.

Tasks is more broader term, but in terms of the extraction, it is used to refer to the exercises that are incorporated into the text of the chapter or section. They are usually is what the reader is asked to do in the text. They might be presented with phrases such as "Reader should verify that ..." or "Reader can show that ...".

Together with exercises and tasks, Gemini must also extract the definitions that are actively referenced in multiple exercises and tasks.

### 2.2. Output top-level structure

Put each section of the book under corresponding heading in the format: `# Chapter [Number]. [Title]. <br>Section [Number]. [Title].`

Definitions come first in the section under the heading `## Definitions`, if present. They are followed by tasks under the heading `## Tasks`. Finally, exercises come last under the heading `## Exercises [SectionNum]`.

### 2.3. Definitions

