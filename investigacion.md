---
layout: page
title: Investigación actual
---

---

Actualmente investigo modelos de equilibrio general bajo incertidumbre donde se intercambian activos contingentes, tratando de encontrar variaciones que expliquen el acertijo del premio al riesgo (*equity premium puzzle*).

El ajuste estadístico del modelo de equilibro general en dos periodos que constituye la parte central de mi tesis se encuentra en [este repositorio](https://github.com/rodrigo-lp/tesis-colmex). El texto de la tesis no está disponible pues aún no se aprueba, aunque la idea general se expone brevemente abajo.

---

## 1. A pure exchange economy

Consider a three-period pure exchange economy. At \\(t=0\\) there is an open market for two types of financial asset: a risky one and a risk-free one. The agents, provided with an initial endowment \\(\omega\\), must find an optimal investment portfolio to transfer its wealth across time (as in an Arrow-Debreu economy). There are two types of agents: *type 1* agents obtain utility from consuming only at \\(t=1\\), while *type 2* agents can freely consume at every period. Type 1 agents can be regarded then as agents who suffer a *consumption shock*, in the form of an illness, an emergency or other non-insured future event. The key insight here is that at time \\(t=0\\) the agents do not know their type, so they must make their investment decisions facing a fundamental uncertainty about their future consumption path. Therefore, the uncertainty in the model comes from two different sources:

1. the intrinsec volatility of the risky asset (the returns of this asset are stochastic), and
1. the risk of being a type 1 agent and be forced to sell the whole portfolio al \\(t=1\\) to achieve maximal utility.

We will assume that the agents estimate a subjetive probability of being type 1 or type 2, namely \\(\pi_1\\) and \\(\pi_2\\) respectively. Therefore, the expected utility of the agent an time zero is

\\[ \pi_1 E_0[u(c_0) + \beta u(c_1)] + \pi_2 E_0[u(c_0) + \beta u(c_1) + \beta^2(c_2)] \\]

which can be reduced to

\\[ E_0[u(c_0) + \beta u(c_1) + \pi_2 \beta^2(c_2)] \\]


## 2. Equilibrium

The equilibrium of this economy is characterized as a Radner equilibrium where the following conditions must hold:

1. Every agent maximises its expected utility subject to the budget constraint.
1. Since there is no production, aggregate consumption equals the sum of the individual initial endowments.
1. Holding assets provide no utility; therefore, every acquired asset must be sold to consume. This implies that the sum over time of the portfolios of every agent must be zero.

In equilibrium, the price \\(q_k\\) of an asset \\(k\\) at time \\(t=0\\) must satisfy:

\\[ q_k = E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} X^k_1 \right] + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} X^k_2 \right] \\]

where \\(X_t\\) is the payoff of the \\(k\\)-th asset a time \\(t\\).

Since \\(q_k\\) is known at time zero, the pricing equation can be also written as

\\[ 1 = E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} R^k_1 \right] + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} R^k_2 \right] \\]

where \\(R^k_t\\) is the gross return of a unit invested at time zero on the asset \\(k\\), at time \\(t\\).


## The equilibrium relationship between assets

Since the latter pricing equation must hold for every asset (including the risk-free one), then the following expression must hold:

\\[ E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} R_1 \right] + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} R_2 \right] = E_0 \left[ \beta \frac{u'(c_1)}{u'(c_0)} \right] R^f_1 + \pi_2 E_0 \left[ \beta^2 \frac{u'(c_2)}{u'(c_0)} \right] R^f_2 \\]

where \\(R_t\\) is the gross return of the risky asset and \\(R^f_t\\) is the gross return of the risk-free asset.

This equation shows the relationship that must hold in equilibrium between the risky asset and the risk-free asset. A risk premium can be derived after specifying a functional form for the utility function and making assumptions about the stochastic processes that governs the return of the risky asset and the aggregate consumption of the economy.