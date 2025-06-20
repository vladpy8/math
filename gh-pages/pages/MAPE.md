$$
 \text{MAPE}_b = \frac{1}{n_b} \sum_i^{n_b} \frac{|T_{i, b} - E_{i,b}|}{T_{i, b}}
$$

$ \text{MAPE}_b $ is $ \text{MAPE} $  of $ b $ -th brand (level of aggregation)

$ E_{i,b} $ is $i$ -th estimate of $b$ -th brand

$ T_{i,b} $ is $i$ -th true sales of $b$ -th brand

Lets imagine you have $ \text{MAPE}_b $ but you want to calculate $ \text{MAPE} $ global for all $i$ without any correspondence to brands ($b$)

$$
\begin{aligned}

 \text{MAPE}_{\text{global}} &= \frac{1}{\sum_b^B n_b } \left( \sum_b^B n_b * \text{MAPE}_b \right) \\

 &= \frac{1}{\sum_b^B n_b } \left( \sum_b^B n_b \left( \frac{1}{n_b} \sum_i^{n_b} \frac{|T_{i, b} - E_{i,b}|}{T_{i, b}} \right) \right) \\

 &= \frac{1}{\sum_b^B n_b } \left( \sum_b^B \sum_i^{n_b} \frac{|T_{i, b} - E_{i,b}|}{T_{i, b}} \right) \\

 &= \frac{1}{N}  \sum_k^{N} \frac{|T_k - E_k|}{T_k}  \\

\end{aligned}
$$

Since

$$
    N = \sum_b^B n_b \\

    \sum_b^B \sum_i^{n_b} ... = \sum_k^N ...
$$

Which exactly equals to what $ \text{MAPE} $ global would be without brands info 
