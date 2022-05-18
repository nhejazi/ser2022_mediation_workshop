# How to choose an estimand: Real-world example {#estimandirl}

## Comparative effectivness of two medications for opioid use disorder (OUD)

\begin{figure}

{\centering \includegraphics[width=1\linewidth]{img/ctndag} 

}

\end{figure}

_Motivation_: Opposite overall treatment effects for homeless versus
nonhomeless participants. This application was explored in detail by
@rudolph2020explaining.

\begin{figure}

{\centering \includegraphics[width=0.75\linewidth]{img/tmleesttotal} 

}

\end{figure}

### Getting specific about the question

To what extent does the indirect effect through mediators of adherence, pain, and
depressive symptoms explain the differences in treatment effects on OUD relapse
for homeless and nonhomeless individuals?

#### What estimand do we want? {-}

- Can we set $M=m$ (i.e., same value) for everyone?
- Are we interested in estimating indirect effects?

$\rightarrow$ So, _not_ controlled direct effect.

- Do we have an intermediate confounder?
 + Yes, and it's important.

$\rightarrow$ So, _not_ natural (in)direct effects.

- So, we're left with the interventional direct and indirect effects.
- Do we want to estimate the path through treatment initiation ($Z$)?
 + Yes, so, _not_ the conditional versions of these effects.
 + Estimands:
   - Direct effect: $\E(Y_{1,G_0} - Y_{0,G_0})$
   - Indirect effect: $\E(Y_{1,G_1} - Y_{1,G_0})$
 + Here $G_a$ is a draw from the distribution of $M_a\mid W$.
- Need to incorporate multiple and continuous mediators

#### What if the positivity assumption $\P(A=a\mid W)>0$ violated? {-}

$\rightarrow$ Can't identify or estimate any of the above effects

- But we can estimate the effect of some stochastic interventions, e.g., IPSIs
- Tradeoff between feasibility and interpretation

#### What if the exposure variable is continuous? {-}

$\rightarrow$ All the above effects are defined for binary exposures

- But we can estimate the effect of some stochastic interventions
- Work in progress (including upcoming R software)