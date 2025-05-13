# Gemini Transcription Prompt: Mathematics

## 0. Core Principles

* **Fidelity:** Transcription must accurately and completely reflect the source material for the specified section(s) only.
* **Output:** Markdown format. No solutions; leave area after `---` blank.
* **Whitespace (CRITICAL):** Exactly one blank line (double newline) must separate every distinct logical block (headings, page numbers, "Let" statements, prose lines, `$$...$$` blocks, `---` separators). No multiple blank lines.

## 1. Document Structure

1.  **Main Heading:** `# Chapter [Num]. [Title]. <br>Section [Num]. [Title].`
	* Example:
		```markdown
		# Chapter 1. Vector spaces. <br>Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $.
		```
2.  **Content Blocks (H2 Headings, In Order):** `## Definitions`, `## Embedded tasks`, `## Exercises [SectionNum]`.
	* Example:
		```markdown
		## Exercises 1C
		```

## 2. Transcribing Definitions

1.  **Heading:** `### [Term Name]`
2.  **Context (Optional):** Single line of plain English if term is broad (e.g., "$ \mathbb{C} $ is set of complex numbers.").
3.  **Page Reference:** On line after heading/context.
4.  **Prerequisites ("Let" statements):** Introduce necessary objects/variables before the main definition, each on its own line, using concise math notation (see Section 5).
	* Example:
		```markdown
		Let $ V_1, \dots, V_m $ be subspaces of $ V $.
		```
5.  **Introductory Prose:** Minimal (e.g., "The [term] is"), on its own line.
6.  **Formal LaTeX Definition:**
	* Use one comprehensive `$$ ... $$` block if possible, encoding properties symbolically (set-builder, quantifiers). Minimize redundant prose. The properties defining the term should be encoded within this LaTeX block rather than reiterated in prose if the LaTeX is sufficiently expressive and clear.
	* Structure multiple aspects (e.g., structure & operations) within one `$$...$$` block using `aligned`, `\\`, `\quad` (see Section 5.1).
	* **Example (Symbolic Definition - Direct Sum):**
		```markdown
		### Direct sum

		Page 21

		Let $ V_1, \dots, V_m $ be subspaces of $ V $.

		The direct sum of $ V_1, \dots, V_m $ is
		$$V_1 \oplus \dots \oplus V_m = \{ v \in V: \quad \exist ! \ v_1 \in V_1, \dots v_m \in V_m, \quad v = v_1 + \dots + v_m \}$$
		```
	* **Example (Structure and Operations - Complex Numbers):**
		```markdown
		### Complex numbers

		$ \mathbb{C} $ is set of complex numbers.

		Page 2

		$$\mathbb{C} = \{ \alpha: \quad \exist! \ a_r, a_i \in \R, \quad \alpha = a_r + a_i \, i \}$$

		where $ i^2 = -1 $.

		$ \forall \alpha, \beta \in \mathbb{C} $, let $ \alpha = a_r + a_i \, i $ and $ \beta = b_r + b_i \, i $.

		Addition and multiplication on $ \mathbb{C} $ are defined by
		$$
		\begin{aligned}
		\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\
		\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i
		\end{aligned}
		$$
		```

## 3. Transcribing Formal Exercises

1.  **Section Page Reference:** After `## Exercises [SectionNum]` heading. Example:
	```markdown
	## Exercises 1C

	Page 24
	```
2.  **Exercise Heading:** `### Exercise [Section].[Num]` (Optional: `. [Descriptive Title]`). Page ref on next line. Example:
	```markdown
	### Exercise 1A.1. Commutativity of addition

	Page 3
	```
3.  **Multi-part:** Use `#### Part [label]` or `#### [Descriptive Sub-heading]`.
4.  **Problem Statement Formatting:**
	* **Quantifiers First:** LaTeX lines with quantifiers (e.g., `$ \forall \alpha, \beta \in \mathbb{C} $`) *must* be the very first part.
	* **"Let" Statements:** For local items, concise, each on its own line.
		* Example:
			```markdown
			Let $ U_a \subseteq F^3 $.
			```
	* **Mathematical Definitions within Problems (Symbolic Set Definitions):** When a "Let" statement introduces a set $U$ (or any mathematical object) whose elements $f$ (or $x, v$, etc.) are described by properties (e.g., "$f$ is differentiable on an interval and satisfies a condition $f'(a) = K f(b)$"), these properties *must* be incorporated directly into the set-builder notation for $U$ within a display LaTeX block (`$$ ... $$`). The prose describing these properties should not be repeated outside the LaTeX block if the LaTeX definition is complete. The subsequent "Then [proposition]" or task statement will then refer to $U$ as defined.
		* Example:
			```markdown
			Let $ U \subseteq \R^{(-4, 4)} $.

			$$U = \{ f \in \R^{(-4,4)} : f \ \text{is differentiable on} \ (-4,4) \ \text{and} \ f'(-1) = 3 f(2) \}$$
			```
		* For multiple related definitions, use separate blocks or `\\` and `\quad` within one. Example:
			```markdown
			Let
			$$
			U = \{ (x,0,0) \in F^3 : x \in F \} \\
			W = \{ (0,y,0) \in F^3 : y \in F \}
			$$
			```
	* **Given Conditions:** List explicitly.
	* **Core Task Wording:**
		* Proofs/Verifications: State proposition declaratively. Omit "Show that...".
			* Example:
				```markdown
				### Exercise 1A.1. Commutativity of addition

				Page 3

				$ \forall \alpha, \beta \in \mathbb{C} $

				$$\alpha + \beta = \beta + \alpha$$
				---
				```
		* Other Imperatives: Retain "Find...", "Determine if...". For "Determine if...", define set, task is implied.
			* Example:
				```markdown
				### Exercise 1C.1

				Page 24

				#### Part a

				Let $ U_a \subseteq F^3 $.

				$$U_a = \{ (x_1, x_2, x_3) \in F^3 : x_1 + 2x_2 + 3x_3 = 0 \}$$
				---
				```
	* Ancillary Page Refs: Before `---`.
	* "Verify Assertions in Example X.Y": Main heading, then `Example X.Y` ref, then `#### Part [label]` for each assertion with its "Let" statements and declarative statement.
5.  **Separator:** `---` (followed by blank line).

## 4. Transcribing Embedded Tasks

1.  **No Duplication:** Omit if explicitly covered by a formal exercise.
2.  **Order:** List in source order.
3.  **Heading:** `### [Source Type] [Num]. [Declarative Description]` (if applicable, else just description). Page ref on next line.
	* Example:
		```markdown
		### Example 1.37. Verification of sum of subspaces in $ F^3 $

		Page 20
		```
4.  **Structure:** Follow formal exercise structure (3.4), using symbolic definitions (Section 2.6, 3.4).
5.  **Multi-part:** Main proposition, `---`, then `#### [Part Title]`, statement, `---` for sub-tasks.
	* Example (Theorem Verification):
		```markdown
		### Theorem 1.40. Verification that sum of subspaces is a subspace

		Page 21

		Let $ V_1, \dots, V_m $ be subspaces of $ V $.

		Then $ V_1 + \dots + V_m $ is a subspace of $ V $.
		---

		#### $ V_1 + \dots + V_m $ contains additive identity
		---
		```
6.  **Separator:** `---` (followed by blank line).

## 5. Mathematical Notation and Formatting

### 5.1. LaTeX Requirements
* **(a) Padding:** Single space inside delimiters: `$ ... $` and `$$ ... $$`.
	* Examples: `$ x \in \R $`, `$$ U = \{ x \in \R \} $$`
* **(b) Internal Spacing:** Use `\quad` for major logical separations (e.g., conditions in set-builder); `\,` for minor (e.g., `$a_i \, i$`).
	* Example (`\quad`): `$$ \{ v \in V: \quad \exist ! \ v_1 \in V_1, \quad v = v_1 + v_m \} $$`
* **(c) Line Breaks (`\\`):** For multi-part definitions/equations in one `$$...$$` block.
	* Example:
		```markdown
		Let
		$$
		U = \{ (x,0,0) \in F^3 : x \in F \} \\
		W = \{ (0,y,0) \in F^3 : y \in F \}
		$$
		```
* **(d) Alignment (`aligned`):** For multi-step derivations or related operations.
	* Example:
		```markdown
		$$
		\begin{aligned}
		\alpha + \beta &= (a_r + b_r) + (a_i + b_i) \, i \\
		\alpha \beta &= (a_r b_r - a_i b_i) + (a_r b_i + a_i b_r) \, i
		\end{aligned}
		$$
		```
* **(e) Symbolic Language:** Use standard LaTeX symbols (`\mathbb{C}`, `\iff`, `\exist !`, `\forall`) over verbose English.

### 5.2. Conciseness
* Prioritize symbolic representation.
* **Definitions:** After minimal "Let"s and intro prose, use one comprehensive `$$ ... $$` block for the full symbolic definition, incorporating properties into the set-builder notation or symbolic statement itself. Avoid redundant prose.
* **"Let" Statements:** Use concise forms: `Let $ U \subseteq F^3 $.`

### 5.3. Source References & Hints
* **Internal References:** If an item refers to another example/page, note it (e.g., `(see Example 1.35)`).
* **Hints/Notes:** Italicized, on own line(s) before `---`. Example: `*Hint: ...*`
