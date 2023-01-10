---
title: Something Funny
author: Keith A. Lewis
institution: KALX, LLC
email: kal@kalx.net
classoption: fleqn
abstract: Path dependent volatility.
...

\newcommand\cat[1]{\mathbf{#1}}

Consider a stochastic volatility model of stock price $(S_t)_{t\ge0}$ 
satisfying $dS_t/S_t = r\,dt + \Sigma_t\,dB$ where $r$ is constant
and $(\Sigma_t)_{t\ge0}$ is an Ito process.

A first guess at path-dependent $\Sigma_t$ might be
$\Sigma^2_t =  (1/t)\int_0^t (dS_s/S_s)^2 = (1/t)\int_0^t \Sigma^2_s\,ds$,
the average realized volatility.

__Exercise__. _Show $\Sigma_t$ is constant_. 

_Hint_: If $d\Sigma = \alpha\,dt + \beta\,dB$ compute $d(t\Sigma^2)$ two ways
to show $\alpha$ and $\beta$ must be 0.

<details><summary>Solution</summary>
Clearly $d(t\Sigma^2) = \Sigma^2\,dt$.
We also have $d(t\Sigma^2) = t\,d\Sigma^2 + \Sigma^2\,dt
= t(2\Sigma\,d\Sigma + (d\Sigma)^2) + \Sigma^2\,dt$.

This shows $0 = 2\Sigma\,d\Sigma + (d\Sigma)^2 = 2\Sigma(\alpha\,dt + \beta\,dB) + \beta^2\,dt$
so $\beta = 0$ and $\alpha = 0$.
</details>

Consider the discrete time version where
$\Sigma^2_n = 1/(t_n - t_0)\sum_{0\le j < n} \Sigma^2_j (t_{j+1} - t_j)$.

Since $\Sigma^2_1 = 1/(t_1 - t_0)\Sigma^2_0(t_1 - t_0)$ we have $\Sigma_1 = \Sigma_0$.
Rinse and repeat until you stop laughing.