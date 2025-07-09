# Markdown math style guidelines

These style guidelines must be used for writing, correcting, or refactoring mathematical content in Markdown format, particularly when it involves MathJax expressions.

## 1. Reusable terms

### 1.1. Statements and expressions

A **statement** refers to a piece of content, including but not limited to:
- a Markdown heading
- one plain text sentence, or a sequence of such sentences
- a plain text sentence with incorporated MathJax inline expressions `$ ... $`
- one MathJax block expression `$$ ... $$`

MathJax blocks may be incorporated into statements together with plain text, but they must be presented at the end of the statement, after the plain text ends.

MathJax inline expressions `$ ... $` may be incorporated into any part of the statement.

An **expression** is a logically and syntactically separate part of a statement. Each statement consists of one or more expressions.

Some statements are *explicitly* defined in this document as **complex statements**. They are composed of multiple sub-statements, each of which must be considered a separate statement.

Each statement within a complex statement must follow the same rules as a regular statement.

### 1.2. Plain text prose

**Plain text**, **words**, or **wording** expressions refer to plain text prose that is not part of MathJax or Markdown expressions or commands.

### 1.3. Math symbols

**Math symbols** refer to any sequence of characters representing mathematical notation, primarily with MathJax. This includes, but is not limited to:
- `$ \mathbb{C} $` for complex numbers
- `$ \mathbb{R} $` for real numbers
- `$ \forall $` for "for all"
- `$ \exists $` for "there exists"
- `$ \in $` for "is an element of"
- `$ \subseteq $` for "is a subset of"
- `$ \{ .. \} $` for set notation
- `$ : $` for "such that"
- `$ \quad $` for quad space
- `$ \ $` for space
- `$ \implies $` for "implies"
- `$ \iff $` for "if and only if"
- `$ , $` for "and" or "as well as"

### 1.4. Math symbols surrogates

**Math symbols surrogates** refer to any short and descriptive plain text representation of a mathematical concept that is well-known but either lacks its own notation or is too complex for concise symbolic expression. Examples include, but are not limited to:
- differentiability
- continuity
- a vector space being a subspace of another vector space

Math symbols surrogates must be incorporated into MathJax expressions using the following format: `$ \text{} $`. For example:
- `$ \text{is differentiable} $`
- `$ \text{is continuous} $`
- `$ \text{subspace of} $`

Consider the `$ \text{} $` format as proper mathematical notation.

### 1.5. Headings

Headings are Markdown [statements](#11-statements-and-expressions) that indicate the structure of the document.

### 1.6. Documents and blocks

A **document** is a collection of statements.

A document **block** is a group of statements that are treated as a single unit. Documents might be divided into blocks. Usually, blocks should start with a heading statement.

## 2. Syntax and semantics

### 2.1. Newlines

Distinguish between **source code** newlines, **MathJax rendered** newlines, and **Markdown rendered** newlines.

#### 2.1.1. Source code newlines

Put double newlines after every statement, except at the end of the document, where a single newline should be used.

Put a single newline before a MathJax block if it is part of a statement and appears at the end of it.

Consider a source code line extensively wide if it exceeds 110 characters, counting every character.

If either the source code of a MathJax block is extensively wide or it already contains `\\` or similar rendered newline expressions, split it into multiple source code lines using single newlines near special logical breakpoint symbols, such as, but not limited to:
- after the first `$$` and before the last `$$`
- before `\\`
- before `:`, `: \quad`, `: \ `, `: \,`
- before `, `, `, \quad`, `, \ `, `, \,`
- after `\begin{...}` and before `\end{...}`
- before the first `$$` if MathJax block is part of a statement at the end of it

If an expression does not contain logical breakpoint symbols for newlines to split on, but is still extensively wide, it might be considered for refactoring in order to split it into multiple lines afterwards and in strict adherence to the other rules of this style guide.

#### 2.1.2. MathJax rendered newlines

MathJax rendered newlines are the newlines that visually appear in the rendered output of MathJax expressions. They are created using `\\` or similar expressions inside MathJax blocks.

Consider a rendered line extensively wide if it exceeds 130 characters after rendering, counting every character.

If the rendered line of a MathJax block is too wide to fit the screen, split it into multiple lines using `\\` or similar rendered newline expressions near certain logical breakpoint symbols, such as, but not limited to:
- before `$ : $`
- before `$ , $`
- before `$ = $ `, or `$ &= $`

Special notation, such as `\begin{aligned} .. \end{aligned}` might be employed together with rendered newlines. A frequent scenario might involve long equations where the first and last lines are short and represent the essence of the equation.

#### 2.1.3. Markdown rendered newlines

Markdown rendered newlines are the newlines that visually appear in the rendered output of Markdown. They are created using either plain source code newlines or the `<br>` expression.

There are no specific rules for Markdown rendered newlines.

### 2.2. Spacing and indentation

Distinguish between **source code** and **MathJax rendered** spacing and indentation.

#### 2.2.1. Source code spacing and indentation

Use tabs for indentation.

Place spaces inside MathJax inline expressions between `$` and the expression itself.

Place spaces inside MathJax block expressions between `$$` and the expression itself, if newline rules are not applied.

Ensure spacing around most symbols or logically separate pieces of MathJax expressions, such as, but not limited to:
- any variable, value, or constant, such as `$ a $`, `$ 1 $`, `$ \pi $`
- any operator, such as `$ + $`, `$ - $`, `$ \cdot $`, `$ / $`, `$ = $`, `$ \neq $`, `$ < $`, `$ > $`, `$ \leq $`, `$ \geq $`
- any logical connector, such as `$ \implies $`, `$ \iff $`, `$ \exists $`, `$ \forall $`
- any punctuation symbol, such as `$ : $`, `$ , $`, `$ ; $`, `$ . $`
- any rendered newline expression or space, such as `$ \\ $`, `$ \quad $`, `$ \ $`,  `$ \, $`

Use spaces outside brackets and parentheses in MathJax expressions, such as `$ ( $`, `$ ) $`, `$ [ $`, `$ ] $`, `$ \{ $`, `$ \} $`. If the internal expression of brackets or parentheses is long and complex, use spaces between the brackets or parentheses and the expression itself.

#### 2.2.2. MathJax rendered spacing and indentation

Use rendered MathJax symbols for spacing after special symbols that are rendered too close to the following expression, such as, but not limited to:
- use `$ \ $` after `$ \exists $`, `$ \exists ! $`
- use `$ \, $` after `$ \forall $`

Use rendered MathJax symbols for spacing after logical breakpoint symbols if the following expression is long and complex, and rendered newline rules are not applied, such as, but not limited to:
- `$ : \quad $`
- `$ , \quad $`

If there are many logical breakpoint symbols and some parts of the expression might be grouped together, then use `$ \, $` or `$ \ $` instead of `$ \quad $` inside these logical groupings. This may include, but is not limited to:
- consecutive variable declarations, such as `$ a \in A, \, b \in B, \, c \in C $`

For very special mathematical variables or constants, which might be mixed with other variables or constants, use `$ \, $` between the special variable and the rest of the expression in operations involving it. This may include, but is not limited to:
- the imaginary unit `$ i $`
- Euler's number `$ e $`, if it is not used in power expressions, such as `$ e^x $`

Do not put spaces around expressions inside `$ \text{ expressions } $`. Always use `$ \ \text{expressions} \ $` instead.

### 2.3. Punctuation

Do not put periods after MathJax blocks.

Do not put periods after Markdown headings.

Use special punctuation symbols to separate logically independent parts of long MathJax block expressions. This may include, but is not limited to:
- `$ : $` with the meaning "such that", "then", or "therefore"
- `$ , $` with the meaning "and" or "as well as"

### 2.4. Capitalization

Never capitalize words after the first word in a statement, except for proper nouns or words that are always capitalized, such as, but not limited to:
- people's names
- names of theorems

### 2.5. Details section

Use details sections to hide proofs of theorems, solutions to exercises or tasks, explanations, etc.

```markdown

<details>
<summary>Proof</summary>

... one or more internal sub-statements ...

</details>

```

Consider a details section as a [complex statement](#11-statements-and-expressions). The internals of the details section consist of one or more internal sub-statements.

Possible details summary titles include, but are not limited to:
- Proof
- Solution

## 3. Compactness and declarative representation

### 3.1. Compact expressions and statements

Reduce the size and number of expressions if possible.

Use [math symbols](#13-math-symbols), [math symbols surrogates](#14-math-symbols-surrogates), and MathJax inline and block expressions instead of [plain text prose](#12-plain-text-prose) if achievable. If an idea can be expressed using math notation, rewrite it accordingly.

Avoid interleaving of plain text prose and MathJax inline expressions. Such occurrence is a strong indicator of a need to refactor the statement. Rewrite, merge, and compress the statement into a MathJax block expression if possible.

Prefer a clear distinction between plain text prose and MathJax expressions. If a statement contains both, prefer to put plain text prose at the beginning of the statement and MathJax expressions at the end of it.

When referencing a name of math entity, place it inside either MathJax inline or block expressions. An acceptable scenario of interleaving plain text prose and MathJax inline expressions is when MathJax inline expressions consist solely of names of math entities.

### 3.2. Compact document

Reduce the size and number of statements if possible.

For major ideas, milestones, concepts, and results, use standalone statements, which means they should encapsulate a single idea or result. This may include, but is not limited to:
- definitions of major complex concepts
- declaration of complex variables, which span multiple expressions
- key theorem statements
- key results
- final answers to tasks or exercises

Intermediate statements may be merged into one, but should conclude with a major intermediate result, which might be referenced further. This includes, but is not limited to:
- derivations of intermediate results
- intermediate steps in proofs of theorems
- intermediate steps in solutions to tasks or exercises
- auxiliary variable declarations
- auxiliary definitions of concepts

### 3.3. Declarative statements and expressions

Avoid imperative statements, expressions, and wording. The "imperative" usually conveys actions, commands, or instructions.

An expression like "[Action] the [Result]" is less preferable to "[Result]". This may include, but is not limited to:
- "[Prove] the [Theorem]" => "[Theorem]"
- "[Show] that [Property] holds" => "[Property]"
- "[Verify] the [Equality]" => "[Equality]"
- "[Explain] the [Result]" => "[Result]"

The actual proof, solution, or explanation is or will be provided in the details section.

However, imperative commands may be unavoidable when the final expression is not yet known, must remain hidden in the details section, or is extremely long, spanning multiple statements that are hard to merge. In such cases, "[Action] the [Result]" should still be rephrased to be as short as possible. This may include, but is not limited to:
- "[Find] the solution for [Equation]" => "Solve [Equation]"
- "[Find] the [Variables] when [Expression] is true" => "Solve for [Variables]: [Expression]"
- "[Verify] if the [Property] holds" => "Verify [Property]"

Some imperative commands might appear declarative but must still be avoided. This may include, but is not limited to:
- "[Proof] of the [Theorem]" => "[Theorem]"
- "[Verification] of the [Property]" => "[Property]"

### 3.4. Main focus of the representation

Clarity is never a goal. Verbosity is never a goal. Strive for compactness, declarativeness, and generality. Yet accuracy must be preserved.

If there is an opportunity to opt out of details and particulars in favor of a more general statement, do so.

Obscure information and omit unnecessary details if it allows for better alignment with these style guidelines.

## 4. Common types of statements

This section describes structures of the most common types of [statements](#11-statements-and-expressions). It is not exhaustive and does not cover all possible cases.

Structures in this section are not styled according to these style guidelines, and are meant to convey high-level meaning. Apply these structures when suitable, and adapt results to these style guidelines afterwards.

Generally, it is preferable to evolve these structures, rather than inventing new ones. Yet, new ones might be invented if absolutely necessary, as long as they follow the same principles as described in these style guidelines.

### 4.1. Variables declarations

[Statements](#11-statements-and-expressions) of this type introduce variables – symbolic representations of mathematical objects of interest. Variables may represent auxiliary, intermediate, preconditioned, or context-specific objects.

Declare variables using the following structures:
- "[Introduction] [Notation]: [Core-Declaration]"
- "[Introduction] [Core-Declaration]"
- "[Core-Declaration]"

"[Introduction]" is a plain text expression, meant to frame the context of the declaration or visually distinguish it. It may consist of such words as, but not limited to:
- "Let", "Consider", "Assume", "Define" or "Declare"
- "In order to achieve this, define"
- "To proceed, let"
- "In this context, declare"

Omit "[Introduction]" in case there is no connection with previous statements and there is no need to visually distinguish the statement from the previous ones.

"[Notation]" is an auxiliary and short MathJax inline expression, meant to introduce variables symbolic names. It may as well contain additional plain text prose expression for names clarification.

If variables are completely defined by the "[Core-Declaration]" and do not require naming clarification, the "[Notation]" may be omitted.

"[Core-Declaration]" is a formal declaration of the variables. There are simple and complex types of declarations.

Simple "[Core-Declaration]" is a short expression introducing variables names, their values, scope or set membership. Use MathJax inline expressions in this case. This may include such expressions as, but not limited to:
- `$ a = value $`
- `$ a, b \in S $`
- `$ \forall c, d \in S $`
- `$ \exists e \in S $`
- `$ U \subseteq V $`

Complex "[Core-Declaration]" introduces object declarations that span multiple interconnected expressions, often divided by `$ , $`, `$ : $`, rendered MathJax newlines, or other separators. Use MathJax block expressions for these declarations. Complex declarations might consist of, but are not limited to:
- Set builder notation, declaring the set of objects along with their properties, representation, and possible operations
- Complex object requiring declaration of their internal structure, such as vectors with interconnected components

### 4.2. Definitions

[Statements](#11-statements-and-expressions) of this type introduce either a new concept or reference well-known ones.

Examples of [definitions](#42-definitions) include, but are not limited to:
- Fields
- Vector spaces
- Topological spaces
- Algebraic structures
- Operations with the above or other mathematical objects

Express references to well-known concepts using statements of the following structures:
- "[Notation] [Short-Description]"
- "[Notation] [Short-Description]: [Core-Definition]"

Express definitions of new concepts using statements of the following structures:
- "[Introduction] [Notation] [Short-Description]: [Core-Definition]"
- "[Introduction] [Notation]: [Core-Definition]"
- "[Introduction] [Short-Description]: [Core-Definition]"
- "[Introduction] [Core-Definition]"
- "[Core-Definition]"

"[Introduction]" and "[Notation]" are similar to those in [variables declarations](#41-variables-declarations), except the "[Notation]" is meant to provide a concise label for the concept being defined. They may be omitted in similar cases as well.

"[Short-Description]" is an auxiliary plain text expression, meant to provide additional clarification of the concept being defined. It may be omitted if the concept is well-known, self-explanatory, or completely defined by the "[Core-Definition]".

"[Core-Definition]" is a formal definition of the concept using a MathJax block expression. It is similar to the "[Core-Declaration]" of complex [variables declarations](#41-variables-declarations), except it is more general and declares an entire concept.

Omit "[Core-Definition]" for well-known concepts based on the context. For example, when key properties are well known, simple, not relevant, or unlikely to be referenced.

### 4.3. Derivations

Derivations are [statements](#11-statements-and-expressions) that encapsulate the process of deriving new knowledge from existing.

Each derivation statement should contain ideas that are interconnected and logically follow each other. Yet, it is important for derivations to maintain [compactness](#31-compact-expressions-and-statements) and not be overly verbose.

Most frequently, it is derivation statements that may contain some imperative wording.

Derivations are expressed using the following structures:
- "[Introduction] [Core-Derivation]"
- "[Introduction] [Short-Description] [Core-Derivation]"
- "[Short-Description] [Core-Derivation]"
- "[Long-Description]"

"[Introduction]" is a plain text expression connecting previous and immediate results with the current one. It may include such words as, but not limited to:
- "Thus,"
- "Therefore,"
- "Hence,"
- "As a result"
- "This leads to:"
- "From the previous statement follows:"

"[Introduction]" may be omitted if "[Short-Description]" is present and together they do not form a coherent and sound statement.

"[Short-Description]" is a short plain text expression acting as a bridge between other statements and the core derivation itself. It may contain references to particular statements or concepts, as well as very short and clear explanations of the ideas behind the derivation.

"[Core-Derivation]" is a formal derivation of the concept using a MathJax block expression.

"[Long-Description]" is a longer and significantly more verbose version of "[Short-Description]" combined with the "[Core-Derivation]", described using plain text prose and math symbols. Use it if and only if it is impossible to represent the derivation in a MathJax block expression inside "[Core-Derivation]".

Each [derivation](#43-derivations) statement must conclude with a compact result expression, which is likely to be referenced later, or conclude the derivation process.

### 4.4. Lemmas

This is a more general [statement](#11-statements-and-expressions) encompassing lemmas, theorems, corollaries, properties, and other similar statements.

Consider a lemma as a [complex statement](#11-statements-and-expressions) with the following structure:
1. "[Definitions](#42-definitions)"
2. "[Variable-Declarations](#41-variables-declarations)"
3. "[Lemma-Result]"
4. "[Proof]"

"[Definitions]" consists of [definitions](#42-definitions) statements. "[Variable-Declarations]" consists of [variables declarations](#41-variables-declarations) statements. These statements may be omitted if the lemma does not require them.

"[Lemma-Result]" is the core statement of the lemma introducing the main result. It is expressed using the following structures:
- "[Introduction] [Short-Description]: [Core-Lemma-Result]"
- "[Short-Description]: [Core-Lemma-Result]"
- "[Core-Lemma-Result]"

"[Introduction]" is a plain text prose expression meant to frame the context of the lemma, connect it with the previous statements as well as visually distinguish it. It may consist of such words as, but not limited to:
- "The following lemma states that"
- "The theorem states that"
- "The following property holds"

Use "[Introduction]" to provide the proper name of the lemma, theorem, or property.

Omit "[Introduction]" if there is no connection with previous statements, no need to provide a proper name, and no need to visually distinguish the statement from the previous ones.

"[Short-Description]" is a short plain text expression naming or framing the lemma. It may also contain a short explanation of the essence of the lemma and an inline version of variable definitions if "[Core-Lemma-Result]" is too long and complex to include them.

"[Core-Lemma-Result]" is a formal expression of the main lemma result using a MathJax block expression. It may consist of a series of expressions connected with punctuation or operators, such as, but not limited to:
- `$ , $`
- `$ : $`
- `$ \implies $`
- `$ \iff $`
- `$ \therefore $`
- rendered MathJax spaces `$ \quad $`, `$ \ $`, `$ \, $`
- rendered MathJax newlines `$ \\ $`

"[Proof]" is a [details section statement](#26-details-section) of the lemma, encapsulating one or more internal statements such as variable declarations, derivations, and possibly other types of statements which together form a proof of the lemma.

### 4.5. Tasks

Tasks are statements that represent exercises, problems, specific instructions, or open questions.

[Tasks](#45-tasks) are a direct generalization of [lemmas](#44-lemmas).

[Tasks](#45-tasks) structure is mirrored from [lemmas](#44-lemmas). Therefore, all the corresponding rules for [lemmas](#44-lemmas) apply here as well.

By and large, tasks should be expressed as complex statements consisting of the following sequence:
1. "[Definitions]"
2. "[Variable-Declarations]"
3. "[Task-Result]" mirrors "[Lemma-Result]" from [lemmas](#44-lemmas)
4. "[Solution]" mirrors "[Proof]" from [lemmas](#44-lemmas)

Certain tasks require an imperative command to be present in the statement. In this case, the imperative command should be placed at the beginning of the "[Task-Result]" as part of an "[Introduction]" and "[Short-Description]" expressions and should be as short as possible. This may include, but is not limited to:
- "Solve [Equation]"
- "Find [Variable]: [Expression]"
- "Seek solution: [Expression]"

If a task does not contain a solution and the context does not imply that one should be present, then the internal statement of the details section of "[Solution]" should be left empty.

## 5. Examples

The good examples comply with these style guidelines. Use them as a reference and for the clarification of these guidelines and rules, if necessary.

### 5.1. Example. Definition of complex numbers

#### 5.1.1. Good example

These definitions are compact and declarative.

Each statement uses a few words at the beginning and a MathJax block expression at the end.

The first MathJax block is the definition of the imaginary unit $ i $.

The second MathJax block is a definition of complex numbers. It uses set builder notation to declare the set of complex numbers and their representation.

The third MathJax block defines the operations of addition and multiplication of complex numbers.

```markdown

### Complex numbers

The imaginary unit $ i $ is defined as:
$$ i^2 = -1 $$

$ \mathbb{C} $ is the set of complex numbers:
$$ \mathbb{C} = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \} $$

$ \forall \alpha, \beta \in \mathbb{C} $:
$$
\begin{aligned}
\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i
\\ \alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i
\end{aligned}
$$

```

### 5.2. Example. Distributivity of multiplication over addition of complex numbers

#### 5.2.1. Bad example

This statement is not compact, not declarative, is too verbose, and contains excessive wording.

It does not follow the newline and spacing styles.

It mixes plain text prose with MathJax expressions.

The header is imperative.

```markdown

### Prove that addition of complex numbers is distributive

Suppose that $\alpha,\beta,\lambda \in \mathbb{C}$. Then $\lambda(\alpha+\beta) = \lambda\alpha +\lambda\beta$.

... (proof omitted) ...

```

#### 5.2.2. Good example

The statements in this example are [compact and declarative](#3-compactness-and-declarative-representation). They contain minimal plain text, relying primarily on math symbols.

This example includes a [theorem declaration statement](#44-theorems) as well as a details section for the proof. The proof consists of one derivation statement.

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
\lambda  (\alpha + \beta) &= (l_r + l_i \, i)((a_r + b_r) + (a_i + b_i) \, i)
\\ &= (l_r(a_r + b_r) - l_i(a_i + b_i)) + (l_r(a_i + b_i) + l_i(a_r + b_r)) \, i
\\ &= (l_r a_r - l_i a_i + l_r b_r - l_i b_i) + (l_r a_i + l_i a_r + l_r b_i + l_i b_r) \, i
\\ &= (l_r a_r - l_i a_i) + (l_r b_r - l_i b_i) + (l_r a_i + l_i a_r) \, i + (l_r b_i + l_i b_r) \, i
\\ &= ((l_r a_r - l_i a_i) + (l_r a_i + l_i a_r) \, i)
	+ ((l_r b_r - l_i b_i) + (l_r b_i + l_i b_r) \, i)
\\ &= \lambda \alpha + \lambda \beta
\end{aligned}
$$

</details>

```

### 5.3. Example. Square root of $ i $

#### 5.3.1. Bad example

```markdown

### Find square roots of $ i $

Find distinct square roots of $ i $.

... (solution omitted) ...

```

#### 5.3.2. Good example

The entire statement represents a single [task statement](#45-tasks) with declaration and solution.

The solution in the details section is composed of a sequence of derivation statements, one naturally following from the other.

The last statement is a verification of the solution, which may be considered an evolved derivation, connecting the solution with the original task.

```markdown

### Square roots of $ i $

Solve for $ \alpha \in \mathbb{C} $:
$$ \alpha^2 = i $$

<details>
<summary>Solution</summary>

$$
\begin{aligned}
(a_r + a_i \, i)^2 &= i
\\ a_r^2 - a_i^2 + 2 a_r a_i \, i &= i
\end{aligned}
$$

One complex number equation leads to two real number equations:
$$
a_r^2 - a_i^2 = 0
\\ 2 a_r a_i \, i = i
$$

From the first equation follows:
$$ |a_r| = |a_i| $$

The second one leads to:
$$
a_r a_i > 0
\\ 2 |a_r| |a_i| = 1
$$

Thus,
$$ |a_r| = |a_i| = \frac{1}{\sqrt2} $$

And finally,
$$ a_r = a_i = \frac{1}{\sqrt2} \quad \text{or} \quad a_r = a_i = - \frac{1}{\sqrt2} $$

The square roots of $ i $ are:
$$
\frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \quad
\\ \text{or} \quad -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i
$$

Verifying:

$$
\begin{aligned}
\left( \frac{1}{\sqrt2} + \frac{1}{\sqrt2} \, i \right)^2
\\ &= \left( \frac{1}{\sqrt2} \right)^2
	+ 2 \left( \frac{1}{\sqrt2} \right) \left( \frac{1}{\sqrt2} \, i \right)
	+ \left( \frac{1}{\sqrt2} \, i \right)^2
\\ &= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2}
\\ &= i
\end{aligned}
$$

$$
\begin{aligned}
\left( -\frac{1}{\sqrt2} - \frac{1}{\sqrt2} \, i \right)^2
\\ &= \left( -\frac{1}{\sqrt2} \right)^2
	+ 2 \left( -\frac{1}{\sqrt2} \right) \left( -\frac{1}{\sqrt2} \, i \right)
	+ \left( -\frac{1}{\sqrt2} \, i \right)^2
\\ &= \frac{1}{2} + \frac{2}{2} \, i - \frac{1}{2}
\\ &= i
\end{aligned}
$$

</details>

```
