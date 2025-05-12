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

	*	Optional descriptive title: Add a descriptive title from the book or a concise summary *only if* the core idea behind the exercise is general enough to be potentially reused or referenced on its own. Otherwise, omit the descriptive title.

	*	If this specific exercise duplicates an embedded task (see IV.1), a note like `(Embedded task also mentioned on Page X)` should be placed on a new line following this exercise's header.

	*	Example (default):
		```markdown
		### Exercise 1A.4
		```

	*	Example (with optional title and duplication note):
		```markdown
		### Exercise 1A.4. Distributivity of multiplication over addition of complex numbers

		(Embedded task also mentioned on Page 3)
		```

3.	Multi-part exercises:

	*	If an exercise has distinct parts explicitly enumerated in the source (e.g., a, b, c, or 1, 2, 3), each part should be introduced with a level-4 heading.

	*	Format: `#### Part [letter/number]` using the same enumeration style as the source.

		*	Example: `#### Part a` or `#### Part 1`

	*	If the source does not use explicit enumeration for sub-tasks but the task naturally breaks down into distinct components (e.g., proving several related statements or answering distinct questions within one exercise number), descriptive level-4 headings can be used if they clearly delineate these components and improve readability. The choice should be guided by whether the sub-task has a clear, concise descriptive name.

		*	Example: `#### Additive identity of $F^S$`

4.	Problem statement:

	*	"Let" statements:

		Introduce all mathematical objects (sets, variables, functions, parameters, etc.) using "Let" statements.

		*	Clearly define the parent set or type for each object.

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

	*	Core task:

		State the main question or proposition of the exercise.

		*	For questions: "Is $U_a$ a subspace of $F^3$?"

		*	For propositions to prove/disprove: "Then $U_a$ is a subspace of $F^4 \iff b=0$." or "Prove that $U$ is a subspace of $V$."

5.	Solution separator:

	*	Use a markdown horizontal rule (`---`) to clearly separate the problem statement from the area where the solution will be written.

6.	Solution placeholder:

	*	A placeholder "TODO" must be added on the line following the `---`.

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

6.	Multi-part embedded tasks:

	*	Follow the same guidelines as for multi-part formal exercises (see Section III.3). The primary task statement can appear directly under the `###` heading if it's the first "part" of a multi-component task.

		*	Example (for verifying Example 1.25 from the book):
			```markdown
			### $F^S$ is a vector space

			Page 14

			Example 1.25

			Let $S$ be a nonempty set.

			Let $F^S$ be the set of functions from $S$ to $F$ with addition and scalar multiplication defined as:

			$$(f+g)(x) = f(x) + g(x)$$

			$$(\lambda f)(x) = \lambda f(x)$$

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

	*	Follow the same guidelines as for formal exercises (Section III.5 and III.6).

## V. Mathematical notation and formatting (applies to all items)

1.	LaTeX for all math:

	All mathematical symbols, variables, expressions, equations, and set definitions must be rendered using LaTeX.

	*	Use inline LaTeX (`$...$`) for symbols within text.

	*	Use display LaTeX (`$$...$$`) for standalone equations or definitions, especially for set-builder notation.

2.	Conciseness:

	Prioritize mathematical symbols and notation over verbose English descriptions.

	*	Example: Use $U \subseteq F^3$ instead of "Let U be a subset of F^3".

3.	Clarity and readability:

	*	Each sentence, header, list item, "Let" statement, mathematical definition (`$$...$$`), and generally each distinct piece of content in the output must be separated from the next by two newlines.

	*	Ensure mathematical definitions in `$$...$$` are typically on their own line(s) for better readability, surrounded by double newlines.

4.	References to source material (within problem description):

	*	If a formal exercise or embedded task refers to a specific example or page in the source book (beyond the main page reference for the exercise set/embedded task itself), include this reference within the problem description.

	*	Example: `(see Example 1.35)` in the problem description.

5.	Hints and notes:

	*	If the source book provides a hint or a special note for an exercise, include it, typically italicized.

	*	Example: `*This exercise is surprisingly harder than Exercise 12...*`
