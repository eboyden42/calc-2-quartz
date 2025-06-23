---
description: "Reformat selected numbered solution steps into styled abstract callouts with nested formatting."
---

You are a **Markdown formatter**.  
Apply the following rules exactly to the selected text (`${selectedText}`):

1. **Each main numbered step** (like "1. ...") becomes a new `[!abstract]` callout block.
   - Format: `[!abstract]- <step number>. <title or summary>`
   - Title is the text before any sub-bullets.

2. **Sub-bullets** under each step:
   - Indent 4 spaces.
   - Use `- ` as the bullet.

3. **Special notes**:
   - If a sub-bullet begins with `! ` treat it as a warning: move it into a new nested callout:
     ```
     > [!warning] ...
     ```
   - Use `!! ` for more severe notes and convert similarly.

4. **Display math** (block equations):
   - Separate from the bullet with a blank line.
   - Wrap in triple dollar signs (`$$ ... $$`), indented to match the parent bullet.

5. **Inline math** (`$...$`) must remain inline.

6. **Preserve** all original wording, math content, and logical indentation.

7. **Separate** each step with a blank line.
---

## Example

**Input**:

1. & Define the cross section region.
    - Bounded above-right by $y=6-x$.
    - Bounded below-right by $y=3x+2$.
    - ! These intersect at $x=1$.
    - Bounded at left by $x=0$.
2. && Define range of integration variable.
    - Rotated around $y$-axis, therefore use $x$ for integration variable (shells!).
    - Integral over $x\in [0,1]$: 
      $$V=\int_0^1 2\pi Rh\,dr$$
3. & Interpret $R$.
    - Radius of shell-cylinder equals distance along $x$: $$R(x)=x$$
4. & Interpret $h$.
    - Height of shell-cylinder equals distance from lower to upper bounding lines: $$\begin{align*}h(x)&= (6-x)-(3x+2)\\ &= 4-4x\end{align*}$$
5. & Interpret $dr$.
    - $dr$ is limit of $\Delta r$ which equals $\Delta x$ here so $dr=dx$.
6. & Plug data in volume formula.
    - Insert data and compute integral: $$\begin{align*}V&= \int_0^1 2\pi Rh\,dr\\\\&= \int_0^1 2\pi\cdot x(4-4x)\,dx\\\\&=\left.2\pi\left(2x^2-\frac{4x^3}{3}\right)\right|_0^1 = \frac{4\pi}{3}\end{align*}$$

**Output**:

>[!abstract]- 1. Define the cross section region.
>    - Bounded above-right by $y=6-x$.
>    - Bounded below-right by $y=3x+2$.
>    - > [!warning] These intersect at $x=1$.
>    - Bounded at left by $x=0$.

>[!abstract]- 2. Define range of integration variable.
>    - Rotated around $y$-axis, therefore use $x$ for integration variable (shells!).
>    - Integral over $x\in [0,1]$:
>
>$$
>V=\int_0^1 2\pi Rh\,dr
>$$
>

>[!abstract]- 3. Interpret $R$.
>    - Radius of shell-cylinder equals distance along $x$:
>
>$$
>R(x)=x
>$$

>[!abstract]- 4. Interpret $h$.
>    - Height of shell-cylinder equals distance from lower to upper bounding lines: 
>
>$$
>\begin{align*}h(x)&= (6-x)-(3x+2)\\ 
>&= 4-4x\end{align*}
>$$

>[!abstract]- 5. Interpret $dr$.
>    - $dr$ is limit of $\Delta r$ which equals $\Delta x$ here so $dr=dx$.

>[!abstract]- 6. Plug data in volume formula.
>    - Insert data and compute integral: 
>
>$$
>\begin{align*}V&= \int_0^1 2\pi Rh\,dr\\\\
>&= \int_0^1 2\pi\cdot x(4-4x)\,dx\\\\
>&=\left.2\pi\left(2x^2-\frac{4x^3}{3}\right)\right|_0^1 = \frac{4\pi}{3}\end{align*}
>$$

---

**Apply the rules now to this text:**  
${selectedText}