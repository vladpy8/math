# Gemini exercises extraction prompt

## 0. Command

Read this prompt and follow the instructions according to the specified command.

Execute either:
1. [Extraction of exercises](#3-extraction-of-exercises) from the source text.
2. Refuse to do anything else.

Prioritize [precision over speed](#1-precision-over-speed).

Adhere to the [style guidelines](#2-style-guidelines).

If provided, focus on the content of the specific exercise(s), task(s), section(s), or chapter(s) of the source text, reading only the specified fragments and ignoring the rest of the source text.

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
- Plain text sentence with incorporated MathJax inline expressions `$ ... $`
- One MathJax block expression `$$ ... $$`

MathJax blocks might be incorporated into statements, but they must be presented at the end of the statement.

MathJax inline expressions `$ ... $` might be incorporated into any part of the statement.

An **expression** is a logically and syntactically separate piece of a statement. Each statement consists of one or more expressions.

Some statements are *explicitly* defined in this prompt to be **complex statements**. They are composed of multiple sub-statements, each of which is considered to be a separate statement.

#### 2.1.2. Plain text prose

**Plain text expressions**, **words**, or **wording** refer to plain text prose that is not part of MathJax or Markdown expressions or commands.

#### 2.1.3. Math symbols

**Math symbols** refer to any sequences of characters representing mathematical notation, primarily with MathJax. This includes, but is not limited to:
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

#### 2.1.4. Math symbols surrogates

**Math symbols surrogates** refer to any short and descriptive plain text prose representation of a math concept that is well known but doesn't have notation on its own or is too complex to be expressed promptly, such as, but not limited to:
- Differentiability
- Continuity
- Vector space being a subspace of another vector space

Incorporate them into math symbolic expressions using the following format: `$ \text{} $`. For example:
- `$ \text{is differentiable} $`
- `$ \text{is continuous} $`
- `$ \text{is a subspace of} $`

Consider the `$ \text{} $` format as a proper math notation.

### 2.2. Syntax and semantics

#### 2.2.1. Newlines

Distinguish between rendered newlines and source code newlines.

Put double newlines after every statement, except at the end of the document where a single newline should be used.

Put a single newline before a MathJax block if it is part of a statement and appears at the end of it.

If the rendered output of MathJax blocks is too wide to fit the screen, split it into multiple lines using `\\` or similar rendered newline expressions. This might be applied near symbols such as, but not limited to:
- after `$ : \\ $`
- after `$ , \\ $`
- before `$ \\ = $ `, or `$ \\ &= $`
- after the logical end of an expression

Special notation might be used, such as `\begin{aligned} .. \end{aligned}` for better readability. Judge based on the context. The most frequent scenario might include long equations where the first and last lines are short and represent the essence of an equation.

If either the source code of a MathJax block is too wide to fit the screen or it already contains `\\` or similar rendered newline expressions, split it into multiple lines using single newlines near special symbols, such as, but not limited to:
- after `$$`
- after `\\`
- after `:`, `: \quad`, `: \ `
- after `, `, `, \quad`, `, \ `
- after `\begin{...}` and before `\end{...}`
- after the last line of the MathJax block
- before `$$` if it is part of a statement at the end of it

If the statement consists of more than 7 lines, replace single newlines with double newlines inside it.

#### 2.2.2. Spacing and indentation

Use tabs for indentation.

Place spaces inside MathJax inline expressions between `$` and the expression itself.

Place spaces inside MathJax block expressions between `$$` and the expression itself, if newline rules are not applied.

Place spaces between MathJax symbols.

Use rendered MathJax symbols for spacing to improve readability between special math symbols and the rest of the expression. This might include, but is not limited to:
- `$ \exist \ $`
- `$ \forall \, $`
- `$ : \quad $`
- `$ , \quad $`

For very special math terms, such as, but not limited to, the imaginary unit `$ i $`, use `$ \, $` between the unit and the rest of the expression in the case of operations involving it.

#### 2.2.3. Punctuation

Do not put dots after MathJax blocks.

Do not put dots after Markdown headings.

Use special punctuation symbols to separate logically independent parts of long MathJax block expressions. This might include, but is not limited to:
- `$ : $` with the meaning "such that", "then", or "therefore"
- `$ , $` with the meaning "and" or "as well as"

#### 2.2.4. Capitalization

Never capitalize words after the first word in a statement, except for proper nouns or words that are always capitalized, such as, but not limited to:
- People's names
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

Possible details summary titles include, but are not limited to:
- Proof
- Solution

#### 2.2.6. Ellipsis

Use an ellipsis `...` to indicate that content is omitted.

### 2.3. Compactness and declarative presentation

#### 2.3.1. Compact symbols

Use math symbols instead of words wherever possible.

#### 2.3.2. Compact statements

Reduce the size and quantity of statements as much as possible.

Merge statements if they are closely related and might be expressed in a single statement. Reiterate and merge as many statements as possible.

Remove words from statements. Use math symbols, surrogates, notation, MathJax inline and block expressions instead. Few words are permitted at the beginning of a statement, or in the course of it if they are absolutely necessary.

An ideal compact statement consists of no words or very few words at the beginning, and a MathJax block expression encompassing multiple interconnected expressions at the end.

#### 2.3.3. Declarative statements and expressions

Avoid imperative statements, expressions, and wording. The "imperative" usually conveys actions, commands, or instructions.

An expression like "[Action] the [Result]" is less preferable than "[Result]". This might include, but is not limited to:
- "[Prove] the [Theorem]" => "[Theorem]"
- "[Show] that [Property] holds" => "[Property]"
- "[Verify] the [Equality]" => "[Equality]"
- "[Explain] the [Result]" => "[Result]"

The actual proof, solution, or explanation is or will be declared in the details section.

However, imperative commands might be unavoidable wherever the final expression is not known yet, must stay hidden in the details section, or is extremely long, spanning multiple statements that are hard to merge. Then, "[Action] the [Result]" might still be rephrased to be as short as possible. This might include, but is not limited to:
- "[Find] the solution for [Equation]" => "Solve [Equation]"
- "[Find] the [Variables] when [Expression] is true" => "Solve for [Variables]: [Expression]"
- "[Verify] if the [Property] holds" => "Verify [Property]"

Some imperative commands might look declarative, but still must be avoided. This might include, but is not limited to:
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
- `$ a, b \in S $`
- `$ \forall c, d \in S $`
- `$ \exists e \in S $`
- `$ U \subseteq V $`

#### 2.4.3. Derivations

Derivations are statements that encapsulate the process of deriving new knowledge from existing statements.

Each derivation statement should contain ideas that are closely interconnected and logically follow each other. Each derivation step should make it apparent how the next step follows from the previous ones.

Most frequently, it is derivations that might contain a bit of imperative wording.

Derivations should be a bit less prioritized with regard to the merging strategy described in [Section 2.3.2](#2-3-2-compact-statements).

Derivations are expressed using the following structures:
- "[Linker] [Core-derivation]"
- "[Short-description] [Core-derivation]"
- "[Long-description]"

"[Core-derivation]" is a formal derivation of the concept using a MathJax block expression.

"[Linker]" is short wording connecting previous and immediate results with the current one. It might include, but is not limited to:
- "Thus,"
- "Therefore,"
- "Hence,"
- "As a result"
- "This leads to:"
- "From the previous statement follows:"

"[Short-description]" is a short plain text expression acting as a bridge between other statements and the core derivation itself. It might contain references to particular statements or concepts, as well as very short and apparent explanations of the ideas behind the derivation.

"[Long-description]" is a longer and significantly more verbose version of "[Short-description]" combined with the derivation itself being described using plain text prose and math symbols. It should be preferred only if it is impossible to represent the derivation in a MathJax block expression of "[Core-derivation]".

#### 2.4.4. Theorems

This is a more general term encompassing theorems, lemmas, corollaries, and other similar statements.

Consider a theorem as a complex statement consisting of a sequence of:
1. "[Definitions]"
2. "[Variable-declarations]"
3. "[Theorem-declaration]"
4. "[Proof]"

"[Definitions]" consists of [Definitions](#2-4-1-definitions) statements. "[Variable-declarations]" consists of [Variables declarations](#2-4-2-variables-declarations) statements.

"[Theorem-declaration]" is a statement that is expressed using the following structures:
- "[Short-description]: [Core-theorem]"
- "[Core-theorem]"
- "Then [Core-theorem]", if "[Definitions]" and "[Variable-declarations]" are introduced

"[Core-theorem]" is a formal expression of the theorem using a MathJax block expression. It might consist of a series of sub-expressions connected with punctuation or operators, such as, but not limited to:
- `$ , $`
- `$ : $`
- `$ \implies $`
- `$ \iff $`

"[Short-description]" is a short plain text expression naming or framing the theorem. It might also contain a short explanation of the essence of the theorem and an inline version of variables definitions if "[Core-theorem]" is too long and complex to include them.

"[Proof]" of a theorem is a statement that is expressed using a details section. A proof consists of one or more internal statements such as variables declarations, derivations, and possibly other types of statements.

#### 2.4.5. Tasks

Tasks are statements that represent exercises, problems, specific instructions, or open questions.

Theorems are a special case of tasks.

By and large, tasks should be expressed as complex statements consisting of a sequence of:
1. "[Definitions]"
2. "[Variable-declarations]"
3. "[Task-declaration]"
4. "[Solution]"

This structure is mirrored from theorems. Therefore, all the rules for theorems apply here as well.

Certain tasks require an imperative command to be present in the statement. In this case, the imperative command should be placed at the beginning of the "[Task-declaration]" statement and should be as short as possible. This might include, but is not limited to:
- "Solve [Equation]"
- "Find [Variable]: [Expression]"

If a task doesn't contain solutions and the context doesn't imply for it to be present, then the internal statement of the details section of "[Solution]" should be replaced by an ellipsis.

### 2.5. Examples

The good examples comply with the style guidelines. Use them as a reference and for derivation of additional implicit guidelines and rules, if necessary.

#### 2.5.1. Example. Definition of complex numbers

##### Good example

These definitions are compact and declarative.

Each statement uses few words at the beginning and a MathJax block expression at the end.

The first MathJax block is the definition of the imaginary unit $ i $.

The second MathJax block is a definition of complex numbers. It uses set builder notation to declare the set of complex numbers and their representation.

The third MathJax block defines the operations of addition and multiplication of complex numbers.

```markdown

### Complex numbers

The imaginary unit $ i $ satisfies:
$$ i^2 = -1 $$

$ \mathbb{C} $ is the set of complex numbers:
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

This statement is not compact, not declarative, is too verbose, and contains excessive wording.

It does not follow the newline and spacing styles.

```markdown

### Prove that addition of complex numbers is distributive

Suppose that $\alpha,\beta,\lambda \in \mathbb{C}$. Then $\lambda(\alpha+\beta) = \lambda\alpha +\lambda\beta$.

... (proof omitted) ...

```

##### Good example

The statements of this example are compact and declarative. It contains no words, but only math symbols.

This example includes a theorem declaration statement as well as a details section for the proof. The proof consists of one derivation statement.

A long line in the first MathJax block is split by a single newline so that the source code fits the screen.

A long line in the second MathJax block is split by double newlines so that both the rendered output and source code fit the screen. Alignment is used to make it more readable and interconnected across lines.

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

The entire statement represents a single task statement with declaration and solution.

The solution in the details section is comprised of a sequence of derivation statements, one naturally following from the other.

The last statement is a verification of the solution, which might be considered an evolved derivation, connecting the solution with the original task.

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

## 3. Extraction of exercises

### 3.1. Command

Read the source text parts which are specified by the [extraction scope](#3-2-2-scope-of-the-extraction).

Identify the [exercises](#3-3-exercises), [embedded exercises](#3-3-4-embedded-exercises), and [relevant definitions](#3-3-2-relevant-definitions).

Extract the relevant [content](#3-3-extraction-content) from the source text.

Rewrite and reiterate as many times as necessary to follow the [extraction rules](#3-extraction-of-exercises).

Provide the [output document](#3-2-3-output-document) as a Markdown file.

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

As any expression, "[Title]" must be a short, descriptive, compact, and declarative.

#### 3.2.5. "[Label]" expressions

"[Label]" is a numeric or symbolic identifier expression referencing particular parts of the content in the source text.

"[Label]" might be provided in the source text, such as, but not limited to:
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

"[Note]" is an optional note that might be used to indicate the type of content. It depends on the context.

#### 3.2.7. Headings

Headings are Markdown heading statements that indicate the structure of the document.

As headings are statements, they must be followed by double newlines.

### 3.3. Extraction content

The output document comprises an ordered sequence of statements.

#### 3.3.1. Sections

The content of each section must be preceded by corresponding heading statements in the format:
1. `# Chapter [Label]. [Title]`
2. `## Section [Label]. [Title]`

Do not adapt the title of the chapter or section to the style guidelines.

Each section block in the output document should consist of the following sub-blocks in order:
1. [Relevant definitions](#3-3-2-relevant-definitions)
2. [Embedded exercises](#3-3-4-embedded-exercises)
3. [Exercises](#3-3-3-exercises)

#### 3.3.2. Relevant definitions

Relevant definitions are complex statements containing definitions that are crucial for declaring or solving the extracted exercises.

Do not extract non-relevant definitions.

All relevant definitions must be presented under the heading `### Relevant definitions`.

Each separate definition or group of relevant and interconnected definitions must be presented as a separate item under its own subheading using the format `#### Definition [Label]. [Title]`. Label definitions numerically.

Each definition item must consist of:
1. [Page reference statement](#3-2-6-page-reference-statements)
2. [Variables declarations](#2-4-2-variables-declarations) statements, if necessary
3. [Definition](#2-4-1-definitions) statements

#### 3.3.3. Exercises

An exercise is a complex statement representing a problem, question, or task from a formal numbered list at the end of a chapter or section in the source text.

Put all exercises under the heading `### Exercises [Label]`, where `[Label]` is the label of the section in the source text.

Put individual exercise items under the subheading `#### Exercise [Label]. [Title]`, where `[Label]` is the label of the exercise in the source text.

"[Title]" is optional and should be omitted if the exercise is a routine application or lacks a single unifying theme.

Each exercise item must consist of:
1. [Page reference statement](#3-2-6-page-reference-statements)
2. [Task](#2-4-5-tasks) statement

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

Solutions and proofs must be omitted. Put an ellipsis within the details section.

#### 3.4.2. Do not imitate the source text

Do not follow the source text in terms of formatting, structure, or content. It is a top priority to follow the [style guidelines](#2-style-guidelines) and [extraction rules](#3-extraction-of-exercises).

#### 3.4.3. Do not duplicate exercises

If an embedded exercise duplicates or has complete overlap with an exercise, omit the contents of the embedded exercise.

Use the following structure for the duplicate embedded exercise:
1. "[Page-reference]" statement
2. "[Exercise-reference]: [Page-reference]" statement

"[Exercise-reference]" is the [Note] expression from a [page reference statement](#3-2-6-page-reference-statements). Use the following format: "See exercise [Label]". Wrap it in a Markdown link to the specified exercise in the output document.

#### 3.4.4. Preserve multi-part exercises

Some exercises might consist of multiple parts. These might be either clear parts of the exercise labeled by the source text or distinguishable sub-theorem or sub-task statements to be proven or solved, according to the context.

"[Multi-part-solution]" exercises are those that contain multiple interconnected parts relevant to a single unifying task statement of the exercise, such as, but not limited to:
- A set of properties to be proven for an object to belong to a certain class
- A set of sub-statements of the theorem to be proven
- A set of well-known steps to be followed in the solution of a task

Each "[Multi-part-solution]" exercise must contain a single task statement. Details sections of such exercises must be split into sub-exercise items.

"[Multi-task]" exercises contain clear labeling of their parts in the source text, such as, but not limited to:
- A, B, C
- 1, 2, 3

"[Multi-task]" exercises must be split into sub-exercise items. In this case, each sub-exercise item must contain its own task statement, as well as a details section.

Consider each sub-exercise item as a complex statement.

Put each sub-exercise item, whether it is in the details section or in the body of the unifying exercise, under its own subheading using the format `##### [Label]. [Title]`.

Do not omit the details section of the unifying exercise. Omit the details section of the sub-exercise items.

#### 3.4.5. Unwrap references

Some exercises might contain references to pieces of content in the source text that are not part of any exercise or definition. In such cases, it is imperative to follow the references and extract the referenced content according to the rules of this prompt.

Extracted content must be relevant to the exercise and must be placed according to the document structure.

### 3.5. Examples

The good examples comply with the style guidelines. Use them as a reference and for derivation of additional implicit guidelines and rules, if necessary.

#### 3.5.1. Example. Key extraction content components

##### Good example

The key fragments presented here comply with the style guidelines. They are compact, declarative, and use MathJax blocks to represent the key mathematical statements.

```markdown

# Chapter 1. Vector spaces

## Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $

### Relevant definitions

#### Definition 1. Complex numbers

... Definitions omitted ...

#### Definition 2. Coordinate vectors $ F^n $

Page reference 6

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

### Exercises 1A

Page reference 10

... Rest of the exercise omitted ...

#### Exercise 1A.2. Associativity of addition of complex numbers

Page reference 10

$ \forall \alpha, \beta, \lambda \in \mathbb{C} $

$$ (\alpha + \beta) + \lambda = \alpha + (\beta + \lambda) $$

<details>
<summary>Proof</summary>
...
</details>

... Rest of the exercises omitted ...

```
