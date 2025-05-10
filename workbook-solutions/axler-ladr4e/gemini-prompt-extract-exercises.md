# Gemini Prompt for Extracting Exercises

This document outlines the preferred style for transcribing mathematics exercises and embedded tasks from a source (e.g., a textbook) into a Markdown format suitable for further work (e.g., adding solutions).

## I. General Document Structure

1.  **Main Heading:** Each section file should begin with a top-level heading indicating the chapter, section number, and section title.
	* Example: `# Chapter 1. Vector spaces. <br>Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $.`
2.  **Subheadings for Content Blocks (Order Matters):**
	* Use `## Definitions` for restating relevant definitions from the section, if any.
	* Use `## Embedded Tasks` for tasks extracted from the main body of the section. These should appear before the formal end-of-section exercises.
	* Use `## Exercises [Section Number]` for the main block of formal, numbered exercises from the end of a book section.
		* Example: `## Exercises 1C`
3.  **Page References:**
	* For formal exercises (under `## Exercises [Section Number]`):
		* Include the page number from the source book on the line immediately following the `## Exercises [Section Number]` heading.
			* Example:
				```markdown
				## Exercises 1C
				page 24
				```

## II. Individual Exercise Formatting (Formal End-of-Section Exercises)

1.  **Exercise Heading:** Each exercise should have a level-3 heading.
	* Format: `### Exercise [Section].[Number]. [Descriptive Title from Book or Concise Summary]`
	* Example: `### Exercise 1A.4. Distributivity of multiplication over addition of complex numbers`
2.  **Multi-Part Exercises:**
	* If an exercise has distinct parts (a, b, c, etc.), each part should be introduced with a level-4 heading.
	* Format: `#### Part [letter]`
	* Example: `#### Part a`
3.  **Problem Statement:**
	* **"Let" Statements:** Introduce all mathematical objects (sets, variables, functions, parameters, etc.) using "Let" statements.
		* Clearly define the parent set or type for each object.
		* Example: `Let $ U_a \subseteq F^3 $.`
		* Example: `Let $ b \in F $.`
	* **Mathematical Definitions:** Define sets, functions, or specific conditions using standard mathematical notation, primarily set-builder notation, enclosed in display LaTeX (`$$...$$`).
		* Example: `$$ U_a = \{ (x_1, x_2, x_3) \in F^3 : x_1 + 2x_2 + 3x_3 = 0 \} $$`
	* **Given Conditions:** If there are explicit conditions or premises for the exercise, list them clearly. Numbered lists can be used if appropriate.
		* Example:
			```markdown
			Given:
			1. $ \forall u, v \in U \implies u+v \in U $
			2. $ \forall u \in U \implies -u \in U $
			```
	* **Core Task:** State the main question or proposition of the exercise.
		* For questions: "Is $U_a$ a subspace of $F^3$?"
		* For propositions to prove/disprove: "Then $U_a$ is a subspace of $F^4 \iff b=0$." or "Prove that $U$ is a subspace of $V$."
4.  **Solution Separator:**
	* Use a Markdown horizontal rule (`---`) to clearly separate the problem statement from the area where the solution will be written.
5.  **Solution Placeholder (Optional):**
	* A placeholder like "TODO prove or disprove $U_a$ is a subspace of $F^3$" can be added immediately after the `---`.

## III. Mathematical Notation and Formatting (Applies to all items)

1.  **LaTeX for All Math:** All mathematical symbols, variables, expressions, equations, and set definitions must be rendered using LaTeX.
	* Use inline LaTeX (`$...$`) for symbols within text.
	* Use display LaTeX (`$$...$$`) for standalone equations or definitions, especially for set-builder notation.
2.  **Conciseness:** Prioritize mathematical symbols and notation over verbose English descriptions.
	* Example: Use $U \subseteq F^3$ instead of "Let U be a subset of F^3".
3.  **Clarity and Readability:**
	* Use newlines liberally to separate distinct logical parts of the problem statement (e.g., each "Let" statement, each mathematical definition, the core task).
	* Ensure mathematical definitions in `$$...$$` are typically on their own line(s) for better readability.
4.  **References to Source Material:**
	* If a formal exercise refers to a specific example or page in the source book, include this reference within the problem description.
	* Example: `(see Example 1.35)` in the problem description.
5.  **Hints and Notes:**
	* If the source book provides a hint or a special note for an exercise, include it, typically italicized.
	* Example: `*This exercise is surprisingly harder than Exercise 12...*`

## IV. Content Focus (Applies to all items)

1.  **Accuracy:** The rewritten task must accurately reflect the original problem or statement from the source.
2.  **Completeness (of Problem):** Ensure all necessary information from the statement is included.
3.  **No Solutions:** The solution part after the `---` must be left blank or contain only a "TODO" placeholder.

## V. Handling Embedded Tasks (Verifications, Proofs, etc. from Main Text)

This section applies to questions, theorems, or statements within the main explanatory text of a book section that are explicitly or implicitly left for the reader to verify, prove, or solve. These should be grouped under a heading like `## Embedded Tasks from Text` (or similar) which appears *before* the `## Exercises [Section Number]` heading.

1.  **Avoid Duplication - Prefer Formal Exercises:**
	* Before transcribing an embedded task, check if it is identical or substantially the same as a formal exercise at the end of the section.
	* If a substantial overlap exists, **do not** create a separate entry for the embedded task.
	* Instead, ensure the corresponding formal exercise (under `## Exercises [Section Number]`) includes a reference to the page where this task was mentioned in the text.
2.  **Order of Appearance:** If an embedded task is unique (not duplicated as a formal exercise), it should be listed and formatted in the order it appears within the source text.
3.  **Identification:**
	* Look for phrases such as "as you should verify", "the proof is left to the reader/exercise", "the reader can verify", "you should verify", "show that...", etc.
	* Identify statements presented as facts where the justification is explicitly deferred to the reader.
4.  **Heading for Embedded Tasks:**
	* Use a level-3 heading (`###`).
	* Provide a very short, declarative description of what the task is about (e.g., `### Commutativity of Complex Multiplication`, `### $F^S$ is a Vector Space`).
	* Place the page number from the source text on the line immediately *following* this heading.
	* If the task directly relates to a numbered Example, Theorem, Proposition, Lemma, Corollary, or a specific unnumbered statement in the book, add this reference on a new line below the page number. Use a format like `Task for Example 1.25` or `Verification of Theorem 3.2`.
	* Examples:
		```markdown
		### $ F^n $ is a Vector Space
		Page 12
		```markdown
		### $ F^S $ is a Vector Space
		Page 14
		Example 1.25
		```markdown
		### Commutativity of Complex Multiplication
		Page 3
		```
5.  **Structure and Formatting:**
	* Follow the same detailed formatting guidelines as for formal exercises (Section II.3, Section III, Section IV).
	* Clearly state all necessary "Let" statements and definitions required to understand and tackle the task.
	* Formulate the core task as a proposition to prove or a question to answer.
	* Use the `---` separator before the (empty) solution part.
6.  **Multi-Part Embedded Tasks:**
	* If an embedded task naturally breaks down into multiple parts (e.g., verifying several bullet points from an example), use level-4 headings (`#### Part [letter]`) for each part, mirroring the style for formal exercises.
		* Example (for verifying Example 1.25 from the book):
			```markdown
			### $F^S$ is a Vector Space
			Page 14
			Example 1.25

			Let $S$ be a nonempty set.
			Let $F^S$ be the set of functions from $S$ to $F$ with addition and scalar multiplication defined as:
			$$(f+g)(x) = f(x) + g(x)$$     $$(\lambda f)(x) = \lambda f(x)$$
			$\forall f, g \in F^S, \forall x \in S, \forall \lambda \in F$.
			Prove that $F^S$ is a vector space over $F$.
			---

			#### Additive Identity of $F^S$
			Let $0_{F^S}: S \to F$ be defined by $0_{F^S}(x) = 0$ for all $x \in S$.
			Prove that $0_{F^S}$ is the additive identity of $F^S$.
			---
			```
