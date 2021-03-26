---
layout: page
title: Investigación actual
---

---

Actualmente investigo modelos de equilibrio general bajo incertidumbre donde se intercambian activos contingentes, tratando de encontrar variaciones que expliquen el acertijo del premio al riesgo (*equity premium puzzle*).

El ajuste estadístico del modelo de equilibro general en dos periodos que constituye la parte central de mi tesis se encuentra en [este repositorio](https://github.com/rodrigo-lp/tesis-colmex). El texto de la tesis no está disponible pues aún no se aprueba, aunque la idea general se expone brevemente abajo.

---

## 1. A pure exchange economy

Consider a three-period pure exchange economy. At \\(t=0\\) there is an open market for two types of financial asset: a risky one and a risk-free one. The agents, provided with an initial endowment \\(\omega\\), must find an optimal investment portfolio to transfer its wealth across time (as in an Arrow-Debreu economy). There are two types of agents: *type 1* agents obtain utility from consuming only at \\(t=1)\\, while *type 2* agents can freely consume at every period. Type 1 agents can be regarded then as agents who suffer a *consumption shock*, in the form of an illness, an emergency or other non-insured future event. The key insight here is that at time \\(t=0)\\ the agents do not know their type, so they must make their investment decisions facing a fundamental uncertainty about their future consumption path. Therefore, the uncertainty in the model comes from two different paths:
1. the intrinsec volatility of the risky asset (the returns of this asset are stochastic), and
1. the risk of being a type 1 agent and be forced to sell the whole portfolio al \\(t=1)\\ to achieve maximal utility.

We will assume that the agents estimate a subjetive probability of being type 1 or type 2, namely \\(\pi_1)\\ and \\(\pi_2)\\ respectively. Therefore, the expected utility of the agent an time zero is
\\[ \pi_1 E_0[u(c_0) + \beta u(c_1)] + \pi_2 E_0[u(c_0) + \beta u(c_1) + beta^2(c_2)] ]\\
which can be reduced to
\\[ E_0[u(c_0) + \beta u(c_1) + \pi_2 beta^2(c_2)] ]\\


## 2. Equilibrium

(Pending)
