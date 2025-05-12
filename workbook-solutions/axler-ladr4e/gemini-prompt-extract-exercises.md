# Gemini prompt for extracting exercises
This document outlines the preferred style for transcribing mathematics exercises and embedded tasks from a source (e.g., a textbook) into a markdown format suitable for further work (e.g., adding solutions).
## I. General document structure
1.	Main heading:
	Each section file should begin with a top-level heading indicating the chapter, section number, and section title.
	*	Example: `# Chapter 1. Vector spaces. <br>Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $.`
2.	Subheadings for content blocks (order matters):
	*	Use `## Definitions` for restating relevant definitions from the section, if any.
	*	Use `## Embedded tasks` for tasks extracted from the main body of the section. These should appear before the formal end-of-section exercises.
	*	Use `## Exercises [Section Number]` for the main block of formal, numbered exercises from the end of a book section.
		*	Example: `## Exercises 1C`
3.	Structure within `## Definitions` section:
	*	Each defined term should be introduced with a `### [Term Name]` subheading.
	*	This can be followed by a brief, plain English description or context for the term on its own line, especially for generally understood concepts (e.g., '$ \mathbb{C} $ is set of complex numbers'). This description is not a "Let" statement.
	*	"Let" statements should be reserved for defining specific objects or notations within the scope of a particular task or example, not for fundamental mathematical entities like $\mathbb{C}$ or $\R$ unless introducing a specific local notation for them (see also Section III.4. "Let" statements).
	*	The formal mathematical definition using LaTeX (`$$...$$`) should then follow.
## II. Content focus (applies to all items)
1.	Accuracy:
	The rewritten task must accurately reflect the original problem or statement from the source.
2.	Completeness (of problem):
	Ensure all necessary information from the statement is included.
3.	No solutions:
	The solution part after the `---` must be left blank. A "TODO" placeholder must be added on the line following the `---` (see III.6 and IV.7).
## III. Individual exercise formatting (formal end-of-section exercises)
1.	Overall section page reference:
	*	Include the page number from the source book on the line following the `## Exercises [Section Number]` heading. This indicates where the set of exercises begins.
		*	Example:
			```markdown
			## Exercises 1C
			Page 24
			```
2.	Exercise heading:
	Each exercise should have a level-3 heading.
	*	Default format: `### Exercise [Section].[Number]`
	*	**Descriptive title (Bias Towards Inclusion):** Lean towards including a descriptive title after the exercise number (e.g., "### Exercise X.Y. Descriptive Title") unless the exercise is an extremely brief and specific computation with no broader conceptual name (e.g., solving a single simple equation). The title should reflect the core mathematical concept being addressed if identifiable.
	*	If this specific exercise duplicates an embedded task (see IV.1), a note like `(Embedded task also mentioned on Page X)` should be placed on a new line following this exercise's header.
	*	Example (default, for a specific computation without a broad conceptual name):
		```markdown
		### Exercise 1A.7
		```
	*	Example (with descriptive title and duplication note):
		```markdown
		### Exercise 1A.1. Commutativity of addition of complex numbers
		(Embedded task also mentioned on Page 3)
		```
3.	Multi-part exercises:
	*	If an exercise has distinct parts explicitly enumerated in the source (e.g., a, b, c, or 1, 2, 3), each part should be introduced with a level-4 heading. Format: `#### Part [letter/number]` using the same enumeration style as the source.
		*	Example: `#### Part a` or `#### Part 1`
	*	If the source does not use explicit enumeration for sub-tasks but the task naturally breaks down into distinct components (e.g., proving several related statements or answering distinct questions within one exercise number), descriptive level-4 headings *can be used instead of* `Part [letter/number]`, provided they clearly delineate these components and improve readability (e.g., `#### Additive identity of $F^S$`).
4.	Problem statement:
	*	**Quantifier statements (Strict Placement):** If an exercise or task in the source begins with a universal or existential quantification of variables (e.g., "$ \forall \alpha, \beta \in \mathbb{C} $"), this LaTeX line *must* be the very first part of the problem statement, preceding any other prose or "Let" statements for that exercise.
	*	**"Let" statements (Contextual Use):** Use "Let" statements primarily for introducing variables, sets, functions, or parameters that are specific to the immediate context of a single exercise or a sub-part of an exercise. General mathematical entities (like $ \mathbb{R} $, $ \mathbb{C} $) should be referred to by their standard symbols.
		*	Clearly define the parent set or type for each object introduced with "Let".
		*	Example: `Let $ U_a \subseteq F^3 $.`
		*	Example: `Let $ b \in F $.`
	*	Mathematical definitions:
		Define sets, functions, or specific conditions using standard mathematical notation, primarily set-builder notation, enclosed in display LaTeX (`$$...$$`).
		*	Example: `$$ U_a = \{ (x_1, x_2, x_3) \in F^3 : x_1 + 2x_2 + 3x_3 = 0 \} $$`
	*	Given conditions:
		If there are explicit conditions or premises for the exercise, list them clearly. Numbered lists can be used if appropriate.
		*	Example:
			```markdown
			Given:
			1.	$ \forall u, v \in U \implies u+v \in U $
			2.	$ \forall u \in U \implies -u \in U $
			```
	*	**Core task (Omission of Imperative Phrases):** If an exercise heading clearly describes the property to be proven (e.g., "Commutativity of X"), the core task should directly state the mathematical proposition as a LaTeX equation, omitting imperative phrases like "Show that" or "Prove that". The context of it being an exercise implies these actions. Retain imperatives for tasks that are not proofs, such as "Solve for x...", "Find...", "Determine if...", "List...", "Describe... (if not asking for a proof)", or similar action-oriented tasks that are not direct synonyms for 'prove'.
		*	Example (declarative):
			```markdown
			### Exercise 1A.1. Commutativity of addition of complex numbers
			$ \forall \alpha, \beta \in \mathbb{C} $
			$$\alpha + \beta = \beta + \alpha$$
			```
		*	Example (imperative if needed): "Solve for $x \in \R^4$."
	*	**Ancillary Page References:** If a specific formal exercise in the source text refers to another page for context or related information (distinct from the main page reference for the exercise set), this reference (e.g., "Also page X") should be included on a new line directly following the exercise problem statement, before the `---` separator.
5.	Solution separator:
	*	Use a markdown horizontal rule (`---`) to clearly separate the problem statement from the area where the solution will be written.
6.	Solution placeholder:
	*	**Mandatory "TODO" Placeholder:** A placeholder "TODO" *must* be added on the line immediately following the `---`.
	*	Example:
		```markdown
		---
		TODO
		```
## IV. Handling embedded tasks (verifications, proofs, etc. from main text)
This section applies to questions, theorems, or statements within the main explanatory text of a book section that are explicitly or implicitly left for the reader to verify, prove, or solve. These should be grouped under a heading like `## Embedded tasks` (or similar) which appears *before* the `## Exercises [Section Number]` heading.
1.	Avoid duplication - prefer formal exercises:
	*	Before transcribing an embedded task, check if it is identical or substantially the same as a formal exercise at the end of the section.
	*	If a substantial overlap exists, **do not** create a separate entry for the embedded task.
	*	Instead, ensure the corresponding formal exercise (under `## Exercises [Section Number]`) includes a reference to the page where this task was mentioned in the text, as described in Section III.2.
2.	Order of appearance:
	If an embedded task is unique (not duplicated as a formal exercise), it should be listed and formatted in the order it appears within the source text.
3.	Identification:
	*	Look for phrases such as "as you should verify", "the proof is left to the reader/exercise", "the reader can verify", "you should verify", "show that...", etc.
	*	Identify statements presented as facts where the justification is explicitly deferred to the reader.
4.	Heading for embedded tasks:
	*	Use a level-3 heading (`###`).
	*	Provide a very short, declarative description of what the task is about (e.g., `### Commutativity of complex multiplication`, `### $F^S$ is a vector space`).
	*	Place the page number from the source text on the line *following* this heading (using uppercase "Page").
	*	If the task directly relates to a numbered Example, Theorem, Proposition, Lemma, Corollary, or a specific unnumbered statement in the book, add this reference on a new line below the page number. Use a format like `Example 1.25` or `Theorem 3.2`.
	*	Examples:
		```markdown
		### $F^n$ is a vector space
		Page 12
		```
		```markdown
		### $F^S$ is a vector space
		Page 14
		Example 1.25
		```
		```markdown
		### Commutativity of complex multiplication
		Page 3
		```
5.	Structure and formatting:
	*	Follow the same detailed formatting guidelines as for formal exercises (Section III.4 for problem statement, Section V for mathematical notation), including the double newline separation.
	*	For internal references: If an embedded task refers to a previous exercise number or a clearly named definition from the source text that has already been transcribed in the current or previous sections, use a textual reference (e.g., "(see Exercise 1A.11)" or "(referencing the definition of complex numbers in Section 1A)").
6.	Multi-part embedded tasks:
	*	Follow the same guidelines as for multi-part formal exercises (see Section III.3). The primary task statement can appear directly under the `###` heading if it's the first "part" of a multi-component task.
		*	Example (for verifying Example 1.25 from the book):
			```markdown
			### $F^S$ is a vector space
			Page 14
			Example 1.25
			Let $S$ be a nonempty set.
			Let $F^S$ be the set of functions from $S$ to $F$ with addition and scalar multiplication defined as:
			$$(f+g)(x) = f(x) + g(x)$$		$$(\lambda f)(x) = \lambda f(x)$$
			$\forall f, g \in F^S, \forall x \in S, \forall \lambda \in F$.
			Prove that $F^S$ is a vector space over $F$.
			---
			TODO
			#### Additive identity of $F^S$
			Let $0_{F^S}: S \to F$ be defined by $0_{F^S}(x) = 0$ for all $x \in S$.
			Prove that $0_{F^S}$ is the additive identity of $F^S$.
			---
			TODO
			```
7.	Solution separator and placeholder:
	*	Follow the same guidelines as for formal exercises (Section III.5 and **III.6 regarding mandatory "TODO"**).
## V. Mathematical notation and formatting (applies to all items)
1.	LaTeX for all math:
	All mathematical symbols, variables, expressions, equations, and set definitions must be rendered using LaTeX.
	*	Use inline LaTeX (`$...$`) for symbols within text.
	*	Use display LaTeX (`$$...$$`) for standalone equations or definitions, especially for set-builder notation.
	*	Prefer simpler, standard LaTeX notation where possible (e.g., `\R` is generally preferred over `\mathbb{R}` if both render acceptably and `\R` is consistently used). For complex numbers, `\mathbb{C}` should be used consistently. Avoid overly specific or obscure LaTeX commands if standard alternatives exist and are clear.
2.	Conciseness:
	Prioritize mathematical symbols and notation over verbose English descriptions.
	*	Example: Use $U \subseteq F^3$ instead of "Let U be a subset of F^3".
3.	Clarity and readability:
	*	**Rigorous Use of Double Newlines:** Each sentence, header, list item, "Let" statement, mathematical definition (`$$...$$`), and generally each distinct piece of content in the output *must* be separated from the next by two newlines. This applies unless the content is part of a single, continuous LaTeX block that uses its own internal line breaking (e.g., an `aligned` environment with `\\`).
	*	Ensure mathematical definitions in `$$...$$` are typically on their own line(s) for better readability, surrounded by double newlines.
4.	References to source material (within problem description):
	*	If a formal exercise or embedded task refers to a specific example or page in the source book (beyond the main page reference for the exercise set/embedded task itself), include this reference within the problem description.
	*	Example: `(see Example 1.35)` in the problem description. (See also Section III.4 regarding ancillary page references for formal exercises).
5.	Hints and notes:
	*	If the source book provides a hint or a special note for an exercise, include it, typically italicized.
	*	Example: `*This exercise is surprisingly harder than Exercise 12...*`
