$$ (a_1 + a_2 + ... + a_p)^n = \sum_{\underset{k_1 \ge 0, k_2 \ge 0, ..., k_p \ge 0}{k_1+k_2+...+k_p = n}} \binom{n}{k_1, k_2, ..., k_p} a_1^{k_1}  a_2^{k_2}  ...  a_p^{k_p} $$

$$  (a_1 + a_2 + ... + a_p + a_{p +1})^n = ? $$

---

$$  (a_1 + a_2 + ... + a_p + a_{p +1})^n = \sum_{k_{p+1}=0}^{n} \binom{n}{k_{p+1}} (a_1 + a_2 + ... + a_p)^{n - k_{p+1}} a_{p+1}^{k_{p+1}}  $$

$$ ... = \sum_{k_{p+1}=0}^{n} \binom{n}{k_{p+1}}(\sum_{\underset{k_1 \ge 0, k_2 \ge 0, ..., k_p \ge 0}{k_1+k_2+...+k_p = n-k_{p+1}}} \binom{n-k_{p+1}}{k_1, k_2, ..., k_p} a_1^{k_1}  a_2^{k_2}  ...  a_p^{k_p}) a_{p+1}^{k_{p+1}}  $$

---

$$ \binom{n}{k_{p+1}} \binom{n-k_{p+1}}{k_1, k_2, ..., k_p} $$

$$ .. = \frac{n!}{k_{p+1}! (n-k_{p+1})!} \frac{(n-k_{p+1})!}{k_1! k_2! ... k_p!} = \frac{n!}{k_1! * k_2! * ... * k_p! * k_{p+1}!} $$

$$ ... = \binom{n}{k_1, k_2, ..., k_{p+1}} $$

---

$$ ... = \sum_{k_{p+1}=0}^{n} \sum_{\underset{k_1\ge 0, k_2 \ge 0, ..., k_p \ge 0}{k_1+k_2+...+k_p = n-k_{p+1}}} \binom{n}{k_{p+1}}  \binom{n-k_{p+1}}{k_1, k_2, ..., k_p} a_1^{k_1}  a_2^{k_2}  ...  a_p^{k_p} a_{p+1}^{k_{p+1}}  $$

$$ ... = \sum_{\underset{k_1 \ge 0, k_2 \ge 0, ..., k_{p+1} \ge 0}{k_1+k_2+...+k_{p+1} = n}} \binom{n}{k_1, k_2, ..., k_{p+1}} a_1^{k_1}  a_2^{k_2}  ...  a_p^{k_p} a_{p+1}^{k_{p+1}}  $$
