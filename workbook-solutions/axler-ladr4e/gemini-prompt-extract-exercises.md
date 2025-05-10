# Style Guide for Rewriting Mathematics Exercises into Markdown

This document outlines the preferred style for transcribing mathematics exercises from a source (e.g., a textbook) into a Markdown format suitable for further work (e.g., adding solutions).

## I. General Document Structure

1.  **Main Heading:** Each section file should begin with a top-level heading indicating the chapter, section number, and section title.
    * Example: `# Chapter 1. Vector spaces. <br>Section 1A. $ \R^n $ and $ {\mathbb{C}}^n $.`
2.  **Subheadings for Content Blocks:**
    * Use `## Definitions` for restating relevant definitions from the section, if any.
    * Use `## Exercises [Section Number]` for the main block of exercises.
        * Example: `## Exercises 1C`
3.  **TODO Lists:** A "TODO" list (e.g., for fixing references) can be included at the beginning of the file if needed.
4.  **Page References:** Include the page number from the source book where the exercises begin.
    * Example: `page 24` (placed directly under the `## Exercises [Section Number]` heading).

## II. Individual Exercise Formatting

1.  **Exercise Heading:** Each exercise should have a level-3 heading.
    * Format: `### Exercise [Section].[Number]. [Descriptive Title from Book or Concise Summary]`
    * Example: `### Exercise 1C.1. Identifying Subspaces in $F^3$`
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

## III. Mathematical Notation and Formatting

1.  **LaTeX for All Math:** All mathematical symbols, variables, expressions, equations, and set definitions must be rendered using LaTeX.
    * Use inline LaTeX (`$...$`) for symbols within text.
    * Use display LaTeX (`$$...$$`) for standalone equations or definitions, especially for set-builder notation.
2.  **Conciseness:** Prioritize mathematical symbols and notation over verbose English descriptions.
    * Example: Use $U \subseteq F^3$ instead of "Let U be a subset of F^3".
3.  **Clarity and Readability:**
    * Use newlines liberally to separate distinct logical parts of the problem statement (e.g., each "Let" statement, each mathematical definition, the core task).
    * Ensure mathematical definitions in `$$...$$` are typically on their own line(s) for better readability.
4.  **References to Source Material:**
    * If an exercise refers to a specific example or page in the source book, include this reference.
    * Example: `Also page 19` or `(see Example 1.35)`.
5.  **Hints and Notes:**
    * If the source book provides a hint or a special note for an exercise, include it, typically italicized.
    * Example: `*This exercise is surprisingly harder than Exercise 12...*`

## IV. Content Focus

1.  **Accuracy:** The rewritten exercise must accurately reflect the original problem from the source.
2.  **Completeness (of Problem):** Ensure all necessary information from the exercise statement is included.
3.  **No Solutions:** The solution part after the `---` must be left blank or contain only a "TODO" placeholder.
