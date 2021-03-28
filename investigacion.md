---
layout: page
title: Investigación actual
---

---

La propuesta de mi tesis, en la cual estoy trabajando actualmente, consiste en un modelo de equilibrio general bajo incertidumbre donde se intercambian activos contingentes. La incertidumbre en el modelo proviene tanto de los posibles estados de la naturaleza (que determinan el retorno de los activos en cada periodo del tiempo) como del supuesto de que los agentes enfrentan información incompleta acerca de sus preferencias de consumo futuras. Así investigo el efecto de eventos inciertos sobre las elecciones óptimas de inversión de los agentes, y trato de determinar si la probabilidad de ocurrencia de dichos eventos (por ejemplo, enfermedades o accidentes para los cuales el agente no está asegurado) puede explicar, al menos en parte, el acertijo del premio al riesgo.

El texto de la tesis se encuentra en revisión. Un esbozo de los fundamentos (aunque incompleto y con ciertas omisiones) se puede leer más abajo. Mientras tanto, el ajuste estadístico del modelo que constituye la parte central del trabajo está disponible en [este repositorio](https://github.com/r-leo/tesis-colmex).

---

### 1. A pure exchange economy

Consider a three-period pure exchange economy. At \\(t=0\\) there is an open market for two types of financial asset: a risky one and a risk-free one. The agents, provided with an initial endowment \\(\omega\\), must find an optimal investment portfolio to transfer its wealth across time (as in an Arrow-Debreu economy). There are two types of agents: *type 1* agents obtain utility from consuming only at \\(t=1\\), while *type 2* agents can freely consume at every period. Type 1 agents can be regarded then as agents who suffer a *consumption shock*, in the form of an illness, an emergency or other non-insured future event. The key insight here is that at time \\(t=0\\) the agents do not know their type, so they must make their investment decisions facing a fundamental uncertainty about their future consumption path. Therefore, the uncertainty in the model comes from two different sources:

1. the intrinsec volatility of the risky asset (the returns of this asset are stochastic), and
1. the risk of being a type 1 agent and be forced to sell the whole portfolio al \\(t=1\\) to achieve maximal utility.

We will assume that the agents estimate a subjetive probability of being type 1 or type 2, namely \\(\pi_1\\) and \\(\pi_2\\) respectively. Therefore, the expected utility of the agent an time zero is

\\[ \pi_1 E_0[u(c_0) + \beta u(c_1)] + \pi_2 E_0[u(c_0) + \beta u(c_1) + \beta^2(c_2)] \\]

which can be reduced to

\\[ E_0[u(c_0) + \beta u(c_1) + \pi_2 \beta^2(c_2)] \\]


### 2. The equilibrium of this economy

The equilibrium of this economy is characterized as a Radner equilibrium where the following conditions must hold:

1. Every agent maximises its expected utility subject to the budget constraint \\(c_t \leq p_t \omega_t + z^k_t X^k_t\\), where \\(X_t\\) is the payoff of the \\(k\\)-th asset a time \\(t\\):
\\[ \max_{z^k_0} \ E_0[u(c_0) + \beta u(c_1) + \pi_2 \beta^2(c_2)] \\]
1. Since there is no production, aggregate consumption equals the sum of the individual initial endowments:
\\[ \sum_i \sum_t c^i_t = \sum_i \sum_t \omega^i_t \\]
where \\(i\\) is the agent index.
1. Holding assets provide no utility; therefore, every acquired asset must be sold to consume. This implies that the sum over time of the portfolios of every agent must be zero:
\\[ \sum_t z^k_t = 0 \\]
for every asset \\(k\\).

In equilibrium, the price \\(q_k\\) of an asset \\(k\\) at time \\(t=0\\) must satisfy:
\\[ q_k = E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} X^k_1 \right] + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} X^k_2 \right] \\]

Since \\(q_k\\) is known at time zero, the pricing equation can be also written as
\\[ 1 = E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} R^k_1 \right] + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} R^k_2 \right] \\]
where \\(R^k_t\\) is the gross return of a unit invested at time zero on the asset \\(k\\), at time \\(t\\).


### 3. An equilibrium relationship between assets

Since the latter pricing equation must hold for every asset (including the risk-free one), then the following expression must hold:

\\[ E_0 \left[ \delta_1 R_1 \right] + \pi_2 E_0 \left[ \delta_2 R_2 \right] = E_0 \left[ \delta_1 \right] R^f_1 + \pi_2 E_0 \left[ \delta_2 \right] R^f_2 \\]

where \\(\delta_t = \beta^t u'(c_t) / u'(c_{t-1})\\), \\(R_t\\) is the gross return of the risky asset and \\(R^f_t\\) is the gross return of the risk-free asset.

This equation shows the relationship that must hold in equilibrium between the risky asset and the risk-free asset. A risk premium can be derived after specifying a functional form for the utility function and making assumptions about the stochastic processes that governs the return of the risky asset and the aggregate consumption of the economy.


### 4. Some key references

#### About the premium puzzle itself

* Abel, Andrew B (1990). "Asset Prices under Habit Formation and Catching up with the Joneses". *The American Economic Review*, 80, pp. 38–42. ISSN 00028282. <http://www.jstor.org/stable/2006539>.
* Brav, Alon; Constantinides, George and Geczy, Christopher (1999). Asset Pricing with Heterogeneous Consumers and Limited Participation: Empirical Evidence. [doi: 10.3386/w7406](https://doi.org/10.3386/w7406).
* Campbell, John Y. (2000). Asset Pricing at the Millennium. *The Journal of Finance*, 55. ISSN 00221082. [doi: 10.1111/0022-1082.00260](https://doi.org/10.1111/0022-1082.00260).
* Campbell, John Y. and Cochrane, John H. (1999). By Force of Habit: A Consumption-Based Explanation of Aggregate Stock Market Behavior. *Journal of Political Economy*, 107. ISSN 0022-3808. [doi: 10.1086/250059](https://doi.org/10.1086/250059).
* Constantinides, G. M.; Donaldson, J. B. and Mehra, R. (2002). Junior Can’t Borrow: A New Perspective on the Equity Premium Puzzle. *The Quarterly Journal of Economics*, 117. ISSN 0033-5533. [doi: 10.1162/003355302753399508](https:/doi.org/10.1162/003355302753399508).
* Constantinides, George M. (1990). Habit Formation: A Resolution of the Equity Premium Puzzle. *Journal of Political Economy*, 98. ISSN 0022-3808. [doi: 10.1086/261693](https://doi.org/10.1086/261693).
* Constantinides, George M and Duffie, Darrell (1996). Asset Pricing with Heterogeneous Consumers. *Journal of Political Economy*, 104, pp. 219–240. ISSN 00223808, 1537534X. <http://www.jstor.org/stable/2138925>.
* DaSilva, Amadeu; Farka, Mira and Giannikos, Christos (2019). Age-Dependent Increasing Risk Aversion and the Equity Premium Puzzle. *Financial Review*, 54. ISSN 0732-8516. [doi: 10.1111/fire.12191](https://doi.org/10.1111/fire.12191).
* Epstein, Larry G and Zin, Stanley E (1991). Substitution, Risk Aversion, and the Temporal Behavior of Consumption and Asset Returns: An Empirical Analysis. *Journal of Political Economy*, 99. [doi: 10.1086/261750](https://doi.org/10.1086/261750).
* Mehra, Rajnish and Prescott, Edward C (1985). The Equity Premium, a Puzzle. *Journal of Monetary Economics*, 15, pp. 145–161.
* Mehra, Rajnish and Prescott, Edward C (2003). The Equity Premium in Retrospect. *Handbook of the Economics of Finance*, pp. 889–938. [doi: 10.1016/S1574-0102(03)01023-9](https://doi.org/10.1016/S1574-0102(03)01023-9).
* Rietz, Thomas A. (1988). The equity risk premium a solution. *Journal of Monetary Economics*, 22. ISSN 03043932. [doi: 10.1016/0304-3932(88)90172-9](https://doi.org/10.1016/0304-3932(88)90172-9).
* Shirvani, Abootaleb; Stoyanov, Stoyan Veselinov; Fabozzi, Frank J. and Rachev, Svetlozar T. (2020). Equity Premium Puzzle or Faulty Economic Modelling? *SSRN Electronic Journal*. ISSN 1556-5068. [doi: 10.2139/ssrn.3530635](https://doi.org/10.2139/ssrn.3530635).
* Wang, Yuanping and Mu, Congming (2019). Can ambiguity about rare disasters explain equity premium puzzle? *Economics Letters*, 183. ISSN 01651765. [doi: 10.1016/j.econlet.2019.108555](https://doi.org/10.1016/j.econlet.2019.108555).
* Wilson, Matthew S. (2020). Disaggregation and the equity premium puzzle. *Journal of Empirical Finance*, 58. ISSN 09275398. [doi: 10.1016/j.jempfin.2020.05.002](https://doi.org/10.1016/j.jempfin.2020.05.002).

#### About the relevance of consumption shocks

* Bunn, Philip; Roux, Jeanne Le; Reinold, Kate and Surico, Paolo (2018). The consumption response to positive and negative income shocks. *Journal of Monetary Economics*, 96. ISSN 03043932. [doi: 10.1016/j.jmoneco.2017.11.007](https://doi.org/10.1016/j.jmoneco.2017.11.007).
* Christelis, Dimitris; Georgarakos, Dimitris; Jappelli, Tullio; Pistaferri, Luigi and van Rooij, Maarten (2019). Asymmetric Consumption Effects of Transitory Income Shocks. *The Economic Journal*, 129. ISSN 0013-0133. [doi: 10.1093/ej/uez013](https://doi.org/10.1093/ej/uez013).
* Karahan, Fatih and Ozkan, Serdar (2013). On the persistence of income shocks over the life cycle: Evidence, theory, and implications. *Review of Economic Dynamics*, 16. ISSN 10942025. [doi: 10.1016/j.red.2012.08.001](https://doi.org/10.1016/j.red.2012.08.001).

#### About the estimation of the model parameters

  * Ahmed, Waqas; Haider, Adnan y Iqbal, Javed (2012). Estimation of discount factor (beta) and coefficient of relative risk aversion (gamma) in selected countries. *MPRA*. <https://EconPapers.repec.org/RePEc:pra:mprapa:39736>.
  * Booij, Adam S. and van Praag, Bernard M.S. (2009). A simultaneous approach to the estimation of risk aversion and the subjective time discount rate. *Journal of Economic Behavior and Organization*, 70, pp. 374–388. ISSN 01672681. [doi: 10.1016/j.jebo.2009.01.005](https://doi.org/10.1016/j.jebo.2009.01.005).
