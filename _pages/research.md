---
permalink: /research/
title: "Research"
author_profile: true
mathjax: true
---
<!-- MathJax for LaTeX Rendering -->
<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$','$$'], ['\\[','\\]']]
  }
};
</script>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js">
</script>

## Independent Projects
### **Pricing Redistribution: Optimal Income Taxation with a Fair-Pricing Constraint**  
*Working Paper in Progress, Oct 2025*  
[View on SSRN →](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5589992)
This paper incorporates the **no-arbitrage condition from financial economics** into the design of optimal income taxation. Workers diversify idiosyncratic wage risk through a variety of institutional and contractual arrangements, suggesting the presence of an implicit *complete market* for wage-contingent claims under the veil of ignorance.

I propose that a social planner’s redistribution scheme—subsidizing or taxing portions of wages contingent on income—can be interpreted as an **option-like contingent claim** tied one-to-one to each unit of labor supplied. For this linkage to hold and to prevent arbitrage, the planner must impose a **fair-pricing constraint** on the redistribution claim, analogous to the no-arbitrage requirement in financial economics. This ensures internal consistency within a complete-market equilibrium.

Within this framework, I begin with a two-bracket system (a wage subsidy plus proportional taxation) and then extend the analysis to a continuous tax schedule. The continuous formulation yields a **correction term** to the standard sufficient-statistics formula, increasing optimal marginal tax rates in proportion to the wedge between *average* and *marginal* rates.

---

## **Fair-Pricing as a Per-Hour Tax Constraint**

I first show that when the risk-free interest rate is zero, the fair-pricing condition can be expressed as an **equivalent constraint on the per-hour tax rate**.

> ### **Lemma 1**
> Let the per-hour tax rate be  
> \( t(n) = T(z_n)/\ell_n \),  
> with \( t(n) \) twice continuously differentiable.
>
> Let \( C(n) \) denote the fair price of a European call option with strike \(n\).
>  
> If a tax schedule \( t_i(n) \) satisfies the fair-pricing constraint, then:
>
> \[
> \int_0^\infty t_i''(n)\, C(n)\, dn = M,
> \]
>
> or equivalently,
>
> \[
> \int_0^\infty t_i(n)\, C''(n)\, dn = 0.
> \]

---

## **Optimal Marginal Tax Rate Under Fair-Pricing**

Adding the fair-pricing constraint to the Mirrlees Hamiltonian yields:

\[
\frac{\tau_n}{1-\tau_n}
=
\frac{A_n + \frac{q}{p}\,\Theta_n}{1 - \frac{q}{p}\,\Theta_n},
\]

where

\[
A_n = \left(1+\frac{1}{e_n}\right)
\frac{\int_{n}^{\infty} (1-\tilde g_m)\, dF(m)}{n f(n)},
\]

\[
\tilde g_m = \frac{G'(u_m)}{p} - \frac{q}{p\,\ell_m},
\]

\[
\Theta_n
= \frac{\ell_n v'(\ell_n) - u_n - v(\ell_n)}{n\ell_n^{2}}.
\]

### **Special Case: Removing the Fair-Pricing Constraint (q = 0)**

When the fair-pricing constraint is removed:

\[
\frac{\tau_n}{1-\tau_n}
=
\left(1+\frac{1}{e_n}\right)
\frac{\int_{n}^{\infty} (1-g_m)\, dF(m)}{n f(n)},
\]

the classical **Diamond (1998)** formula.

---


## **Key Simulation Results**

Simulations under a log-normal skill distribution show that enforcing fair-pricing **flattens the optimal marginal tax schedule**, consistent with empirical tendencies toward flatter schedules in advanced economies.

### **Figure 1. Average–Marginal Tax Gap Before Applying Fair-Pricing**

Panel A shows the classical Mirrlees–Diamond result: marginal tax rates decline with income because the hazard ratio \((1-H)/(z h)\) is decreasing under a lognormal distribution.

Panel B shows that **the no-arbitrage condition** introduces a pseudo(first order) correction term that is:
- **negative** for low-income workers
- **positive** for high-income workers  

indicating that the traditional framework can over-tax low-income households relative to high-income ones.

![Figure Preview](../assets/1by2.png)

---

### **Figure 2. Marginal Tax Schedules Under Increasing λ**

As the shadow value \( \lambda \) of the fair-pricing constraint increases from 0 to 2:

- The marginal tax schedule becomes **progressively flatter**  
- Eventually displays a mild **inverted U-shape**  
- The magnitude of flattening depends on  
  \(\lambda \cdot \Theta_n\),  
  which links average and marginal taxation through the fair-pricing term

![Figure Preview](../assets/2by2.png)

---

### **Labor Hour Spillovers and Educational Spending: Evidence from Korea’s Work-Hour Reform**  
*Working Paper in Progress, Apr 2025*    

[View on SSRN →](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5214642)  

In 2018, the South Korean government implemented a 52-hour work-week limit to curb excessive working hours, initially targeting large enterprises with 300 or more employees. This policy provides a quasi-natural experiment introducing exogenous variation in labor hours among large-firm employees, which in turn influences workers in small and medium-sized enterprises (SMEs) to adjust their labor supply and household behavior in response to new industry-wide norms.  

## Table: First-stage estimation using an instrumental variable

|                         | (1)        | (2)        | (3)        |
|-------------------------|------------|------------|------------|
| **β₀**                  | -2.74***   | -1.68*     | -1.90      |
| **s.e.**                | (0.55)     | (0.67)     | (0.78)     |
| **Time trend**          | No         | Yes        | No         |
| **Time fixed effects**  | No         | No         | Yes        |
| **Observations**        | \multicolumn{3}{c}{1,121} |

**Notes:**  
Estimated standard errors are cluster-robust, clustered at the industry level.  
Industry and job-type fixed effects correspond to the Korea Standard Industry Classification (KSIC) and the Korea Standard Classification of Occupations (KSCO), respectively.  
Control variables include age, age squared, education level, region fixed effects, spouse’s employment status, transfer income, the number of children, and the number of children under six.  
`***`, `**`, and `*` denote significance at the 1%, 5%, and 10% levels, respectively.

Using panel data from the _Korean Labor & Income Panel Study_, I identify a spillover effect whereby reductions in working hours at large firms indirectly reduce labor hours among SME employees. 

## Table: Second-stage least squares estimation using an instrumental variable

|                         | **50–299 Employees** |               | **5–49 Employees** |               |
|-------------------------|-----------------------|---------------|---------------------|---------------|
|                         | (1)                   | (2)           | (3)                 | (4)           |
| **β**                   | 1.43***               | 1.17*         | 0.79***             | -0.15         |
| **s.e.**                | (0.40)                | (0.86)        | (0.17)              | (0.71)        |
| **Time trend**          | No                    | Yes           | No                  | Yes           |
| **Observations**        | 1,380                 | 1,380         | 2,120               | 2,120         |

**Notes:**  
Estimated standard errors are cluster-robust, clustered at the industry level.  
The second-stage estimation includes all explanatory variables from the first stage.  
`***`, `**`, and `*` denote significance at the 1%, 5%, and 10% levels, respectively.  
The F-statistic of the first-stage instrument is significant across all specifications.

This contraction in labor supply also crowds out household educational spending. 

## Table: Two-stage least squares estimation of educational spending

|                                         | 5–299 Employees |               |               |               |
|-----------------------------------------|:---------------:|:-------------:|:-------------:|:-------------:|
|                                         | (1)             | (2)           | (3)           | (4)           |
| **β**                                   | -0.24**         | 0.12          | -0.05         | 0.24          |
| **s.e.**                                | (0.11)          | (0.34)        | (0.04)        | (0.32)        |
| **δ (L<sub>it</sub> × Kids)**           | 0.16***         | 0.12**        | --            | --            |
| **s.e.**                                | (0.06)          | (0.05)        | --            | --            |
| **δ (L<sub>it</sub> × Kids &lt; 6)**    | --              | --            | 0.14**        | 0.13*         |
| **s.e.**                                | --              | --            | (0.06)        | (0.07)        |
| **Time trend**                          | No              | Yes           | No            | Yes           |
| **Observations**                        | 1,788           | 1,788         | 1,788         | 1,788         |
| **First stage F-statistic**             | 233.5           | 58.9          | 122.0         | 71.8          |

**Notes:**  
Estimated standard errors are cluster-robust, clustered at the industry level.  
The second-stage estimation includes all explanatory variables from the first stage.  
`***`, `**`, and `*` denote significance at the 1%, 5%, and 10% levels, respectively.  
The joint F-statistic for the first-stage instruments, including the interaction term,  
is reported for all model specifications.

---
## Publications in NABO (National Assembly Budget Office, Republic of Korea)

### Disaster Insurance Implementation and Financial Management Analysis  
**Solo-authored**.  _Included as the fifth chapter in NABO Comprehensive Analysis on Disaster and Safety Management, 2017_  

[View Translated Summary (PDF)](../files/Disaster_Insurance.pdf)  
[View Full Paper (In Korean)](https://nabo.go.kr/system/common/JSPservlet/download.jsp?fCode=33314430&fSHC=&fName=%EC%9E%AC%EB%82%9C%EC%95%88%EC%A0%84%EA%B4%80%EB%A6%AC+%ED%98%84%ED%99%A9%EA%B3%BC+%EC%A3%BC%EC%9A%94%EB%8C%80%EC%B1%85+%EB%B6%84%EC%84%9D+5.%EC%9E%AC%EB%82%9C%EB%B3%B4%ED%97%98+%EC%9A%B4%EC%98%81%EC%8B%A4%ED%83%9C+%EC%9E%AC%EC%A0%95%EC%9A%B4%EC%9A%A9+%EB%B6%84%EC%84%9D.pdf&fMime=application/pdf&fBid=19&flag=bluenet)  

> - Applied logistic regression to the Farm and Fishery Household Survey to assess distributional impacts of disaster insurance programs.
> - Conducted simulation analyses fitting exponential and mixed-gamma distributions to historical loss ratios to estimate fiscal losses under an actuarially benevolent national reinsurance scheme.

---

### Potential Risks from COVID-19 Responses and Liquidity Expansion  
**With Ick Jin (NABO) et al.**. _Published as a standalone report, National Assembly Budget Office, 2021._  

[View Translated Summary (PDF)](../files/Major_Countries.pdf)  
[View Full Paper (In Korean)](https://nabo.go.kr/system/common/JSPservlet/download.jsp?fCode=33316891&fSHC=&fName=2021%EB%85%84+%EC%A3%BC%EC%9A%94%EA%B5%AD+%EA%B2%BD%EC%A0%9C+%ED%98%84%ED%99%A9+%EB%B6%84%EC%84%9D.pdf&fMime=application/pdf&fBid=19&flag=bluenet)  

> - Conducted a comparative analysis of fiscal policy responses across countries.

---

### Employment Conditions in Small and Medium-Sized Cities  
**Solo-authored**. _NABO Industrial Trends & Issues, Vol. 3, No. 6, 2018, pp.25–37._  

[View Translated Summary (PDF)](../files/Employment_Conditions.pdf)  
[View Full Paper (In Korean)](https://nabo.go.kr/system/common/JSPservlet/download.jsp?fCode=33314781&fSHC=&fName=NABO+%EC%82%B0%EC%97%85%EB%8F%99%ED%96%A5+%26+%EC%9D%B4%EC%8A%88+%28%EC%A0%9C6%ED%98%B8%29.pdf&fMime=application/pdf&fBid=63&flag=bluenet)  

> - Applied linear probability and Heckman selection models using microdata from the Regional Employment Survey to analyze employment and wage disparities between population-growing and population-declining cities.


---



