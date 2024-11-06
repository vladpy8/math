---
layout: new-page
title: "Uncommon Limits"
---

{% include mathjax.html %}

---

#### <cite>Фихтенгольц, Том 1, Глава вторая, параграф 77, страница 184</cite>

<br/>

$$ \lim_{\alpha \to 0}{\frac{\log_{b}{(1 + \alpha)}}{\alpha}} = log_{b}{e} \tag{0} $$

$$ \alpha \in R, \alpha > 0 $$

$$ b \in R, b > 0 $$

<details>
<summary>Proof</summary>

By moving power inside the logarithm one gets

$$
	\lim_{\alpha \to 0}{\frac{\log_{b}{(1 + \alpha)}}{\alpha}}
	= \lim_{\alpha \to 0}{\log_{b}((1 + \alpha)^{1 / \alpha})}
$$

The well-known limit manifestation is

$$ \lim_{\alpha \to 0}{(1 + \alpha)^{1 / \alpha}} = e $$

Using continuity property of the logarithm function as well as continuity and limit value of its argument leads to

$$ \lim_{\alpha \to 0}{\log_{b}{(1 + \alpha)^{1 / \alpha}}} = \log_{b}{e} $$

</details>

<br/>

---

$$ \lim_{\alpha \to 0}{\frac{x^{\alpha} - 1}{\alpha}} = \ln{x} $$

$$ \alpha \in R, \alpha > 0 $$

$$ x \in R, x > 0 $$

<details>
<summary>Proof</summary>

Defining variable

$$ x^{\alpha} - 1 = \beta $$

$$ \alpha = \log_{x}{(1 + \beta)} $$

$$ \beta \in R, \beta > -1 $$

Replacing

$$ \lim_{\alpha \to 0} ({x^{\alpha} - 1}) = \lim_{\alpha \to 0} \beta = 0 $$

Performing same replacement in target limit

$$ \lim_{\alpha \to 0} \frac{ x^{\alpha} - 1 }{ \alpha } = \lim_{\beta \to 0} \frac{ \beta }{ log_{x}{(1 + \beta)} } $$

Given the limit above

$$ \lim_{\beta \to 0} \frac{ \beta }{ log_{x}{(1 + \beta)} } = \frac {1} {log_{x}{e}} = ln{(x)} $$

</details>

<br/>

---

$$ \lim_{\alpha \to 0} \frac{ (1 + \alpha)^p - 1 }{ \alpha } = p $$

<details>
<summary>Proof</summary>

Replacing variable

$$ (1 + \alpha)^p - 1 = \beta $$

$$ p * ln(1 + \alpha) = ln(1 + \beta) $$

Leads to

$$ \lim_{\alpha \to 0}{( (1 + \alpha)^p - 1 )} = \lim_{\alpha \to 0} \beta = 0 $$

Rearranging target expression

$$
	\frac{(1 + \alpha)^p - 1}{\alpha} = \frac{\beta}{\alpha}
	= \frac{\beta}{ln(1 + \beta)} * p * \frac{ln(1 + \alpha)}{\alpha}
$$

Given the limits above

$$ \lim_{\alpha \to 0}{\frac{ln(1 + \alpha)}{\alpha}} = 1 $$

$$ \lim_{\alpha \to 0}{\frac{ln(1 + \beta)}{\beta}} = \lim_{\beta \to 0}{\frac{ln(1 + \beta)}{\beta}} = 1 $$

Thus

$$ \lim_{\alpha \to 0}{\frac{(1 + \alpha)^p - 1}{\alpha}} = 1 * p * 1 $$

</details>

<br/>

---

#### <cite>Фихтенгольц, Том 1, Глава вторая, параграф 62, страница 157</cite>

$$ \lim_{x \to +\infty} \frac{a^x}{x^k} = +\infty $$

$$ \lim_{x \to +\infty} \frac{x^k}{\log_{a}{x}} = \infty $$

<details>
<summary>Proof</summary>

</details>

<br/>
