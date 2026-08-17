# Writing Primer: Markdown and LaTeX

This short primer introduces the two text-formatting tools used in the source files for this course:

- **Markdown** for headings, paragraphs, lists, links, and emphasis
- **LaTeX** for mathematical symbols and equations

This is **not a programming primer**. You are not expected to learn Python or complete coding assignments in PHYS 1401. The purpose of this page is to help you read the course source files and format a clear scientific explanation when Markdown or LaTeX is useful.

You should return to this page whenever you need a quick formatting reference.

---

## Writing in Markdown

Markdown is a lightweight way to organize plain text. The symbols remain readable in the source file and are converted into formatted text when the book is built.

### Headings

Use one or more number signs to create headings.

```md
# Main Title
## Section
### Subsection
```

Use headings to organize ideas, not merely to make text larger.

### Paragraphs and Line Breaks

Separate paragraphs with a blank line.

```md
This is the first paragraph.

This is the second paragraph.
```

A paragraph should usually develop one main idea. In a physics solution, begin a new paragraph when you move from the model to the calculation or from the calculation to the interpretation.

### Emphasis

```md
*italic text*

**bold text**
```

Use italics for light emphasis and bold text for labels or especially important terms. Avoid bolding entire paragraphs.

### Lists

Use hyphens for an unordered list.

```md
- Identify the known quantities.
- Draw a diagram.
- Choose a physical principle.
- Solve and interpret the result.
```

Use numbers when the order matters.

```md
1. Define the system.
2. Choose a coordinate direction.
3. Write the general equation.
4. Substitute numerical values.
```

### Links

```md
[OpenStax College Physics 2e](https://openstax.org/books/college-physics-2e/pages/preface)
```

Use descriptive link text rather than phrases such as “click here.”

### Block Quotations

Use a greater-than sign for a short quotation or highlighted statement.

```md
> A numerical answer is incomplete until its physical meaning is explained.
```

### A Problem-Solving Structure

A complete written solution can be organized with Markdown headings.

```md
### The Problem

State what must be determined.

### The Model

Describe the system, assumptions, diagram, and physical principle.

### The Math

Develop the general equation, solve algebraically, and then substitute values with units.

### The Conclusion

State the result and explain what it means physically.
```

The headings do not replace the explanation. Each section should contain complete thoughts that another person can follow.

#### Mini Exercise

Write a Markdown subsection titled **Strategy** followed by a numbered list containing three steps for solving a physics problem.

````{admonition} Solution
:class: dropdown

```md
## Strategy

1. Identify the known and unknown quantities.
2. Choose the physical principle that connects them.
3. Solve the equation and check whether the result is reasonable.
```
````

---

## Mathematics with LaTeX

LaTeX is used to typeset mathematical expressions. In Markdown, mathematics is placed between dollar signs.

### Inline Mathematics

Use one dollar sign on each side when an expression belongs inside a sentence.

```md
The average speed is $v_{\rm avg}=d/\Delta t$.
```

Rendered:

The average speed is $v_{\rm avg}=d/\Delta t$.

### Displayed Equations

Use two dollar signs on each side when an equation should appear on its own line.

```md
$$
v_{\rm avg}=\frac{d}{\Delta t}.
$$
```

Rendered:

$$
v_{\rm avg}=\frac{d}{\Delta t}.
$$

Do not use display mathematics for every short symbol. Reserve it for equations that deserve visual emphasis or are part of a calculation.

---

## Common LaTeX Patterns

### Subscripts and Superscripts

```md
$x_0$, $v_f$, $t^2$, and $10^{-3}$
```

Rendered: $x_0$, $v_f$, $t^2$, and $10^{-3}$.

Use braces when a subscript or superscript contains more than one character.

```md
$v_{\rm avg}$ and $a_{\rm net}$
```

Rendered: $v_{\rm avg}$ and $a_{\rm net}$.

### Fractions

```md
$\frac{\Delta x}{\Delta t}$
```

Rendered: $\frac{\Delta x}{\Delta t}$.

### Square Roots

```md
$\sqrt{2gh}$
```

Rendered: $\sqrt{2gh}$.

### Greek Letters

```md
$\alpha$, $\theta$, $\Delta$, $\omega$, and $\mu$
```

Rendered: $\alpha$, $\theta$, $\Delta$, $\omega$, and $\mu$.

Remember that uppercase and lowercase Greek letters can represent different quantities.

### Multiplication and Scientific Notation

```md
$F=ma$

$3.2\times10^5\ {\rm m}$
```

Rendered: $F=ma$ and $3.2\times10^5\ {\rm m}$.

Use `\times` for scientific notation rather than a lowercase letter x.

### Trigonometric Functions

```md
$F_x=F\cos\theta$

$F_y=F\sin\theta$
```

Rendered: $F_x=F\cos\theta$ and $F_y=F\sin\theta$.

Standard function names such as `\sin`, `\cos`, and `\tan` are typeset upright automatically.

### Vectors

```md
$\vec{F}$, $\vec{v}$, and $\Delta\vec{x}$
```

Rendered: $\vec{F}$, $\vec{v}$, and $\Delta\vec{x}$.

Use the vector symbol when direction is important. Use an ordinary symbol such as $F$ for the magnitude.

### Units

Keep units outside fractions and variables when practical.

```md
$v=20\ {\rm m/s}$

$a=9.80\ {\rm m/s^2}$
```

Rendered: $v=20\ {\rm m/s}$ and $a=9.80\ {\rm m/s^2}$.

A small space, written as `\ `, separates the number from the unit.

---

## Writing a Calculation Clearly

A calculation should show the general relationship before numerical substitution.

```md
$$
v_{\rm avg}=\frac{\Delta x}{\Delta t}.
$$

Substituting the measured values gives

$$
v_{\rm avg}
=\frac{80\ {\rm m}}{4.0\ {\rm s}}
=20\ {\rm m/s}.
$$
```

This presentation makes the physical model visible and keeps the units attached to the values.

For several connected lines, use an aligned environment.

```md
$$
\begin{aligned}
v_f^2 &= v_0^2+2a\Delta x,\\
v_f &= \sqrt{v_0^2+2a\Delta x},\\
v_f &= 12.4\ {\rm m/s}.
\end{aligned}
$$
```

Rendered:

$$
\begin{aligned}
v_f^2 &= v_0^2+2a\Delta x,\\
v_f &= \sqrt{v_0^2+2a\Delta x},\\
v_f &= 12.4\ {\rm m/s}.
\end{aligned}
$$

Use alignment to show logical steps, not to hide skipped algebra.

### Mini Exercise

Write the equation for the magnitude of a vector with components $A_x$ and $A_y$.

````{admonition} Solution
:class: dropdown

```md
$$
A=\sqrt{A_x^2+A_y^2}.
$$
```
````

---

## Combining Words and Equations

Equations should be part of complete sentences.

Weak:

```md
$$
F=ma
$$
```

Stronger:

```md
Newton's second law relates the net force to the acceleration:

$$
F_{\rm net}=ma.
$$

Because the mass is positive, the acceleration points in the same direction as the net force.
```

Punctuation still belongs at the end of an equation when the equation completes a sentence.

---

## Common Mistakes to Avoid

- Omitting a closing dollar sign
- Using a letter x instead of `\times` for multiplication
- Forgetting braces in expressions such as `v_{avg}`
- Writing units as though they were variables
- Dropping units during numerical substitution
- Presenting equations without explaining why they apply
- Substituting numbers before developing the general relationship
- Using headings or bold text in place of a real explanation

---

## What You Are Expected to Know

For this course, you should be able to:

- recognize the basic Markdown structure used in the course notes,
- format headings, lists, emphasis, and links when needed,
- read common LaTeX expressions,
- type simple inline and displayed equations,
- include subscripts, superscripts, fractions, roots, vectors, and units,
- and combine equations with clear written reasoning.

You are not expected to write computer programs. Markdown and LaTeX are included because they help present physics clearly.
