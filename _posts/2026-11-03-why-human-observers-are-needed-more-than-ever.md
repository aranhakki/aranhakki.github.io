---
layout: post
title: "Why Human Observers Are Needed More Than Ever"
author: "Aran Hakki, MEng, PhD"
---

I believe growing complexity in modern software systems cannot simply fit into the heads of a few senior engineers. Systems thinking tells us that complexity needs to be shared and expanded across all levels of an organization, from junior to senior. 
There is a common narrative that AI is going to eliminate the need for software engineers, but the current hiring bottleneck isn't a lack of work—it's that companies don't yet understand how to work with LLMs effectively. 
When we analyze how to effectively build with AI, the true productivity unlock comes from separating routing from generation. By using Joint Embedding (JEV) architectures for semantic routing and intent to traditional deterministic programs, and keeping non-JEV models strictly for syntax-constrained pattern filling, we create far more reliable workflows, and therefore remove the uncertainty in knowing how best to leverage AI...

According to [Jevons Paradox](https://en.wikipedia.org/wiki/Jevons_paradox), when a technology makes a resource more efficient to produce, we don't end up using less of it—we use far more. Making code generation easier means we will end up building much larger, far more interconnected systems. 

In cybernetics, this phenomenon is governed by [Ashby’s Law of Requisite Variety](https://en.wikipedia.org/wiki/W._Ross_Ashby#Requisite_variety). Formulated by W. Ross Ashby, it dictates that for an observer or controller $O$ to stabilize a system $S$, the internal variety (the number of possible states and observational capacity) of the observer $V(O)$ must match or exceed the variety of the system $V(S)$:

$$
V(O) \ge V(S)
$$

- $V(S)$ represents total system state complexity, which explodes exponentially under AI-driven code generation.
- $V(O)$ represents the internal observational capacity of the human engineering team.

As AI expands system complexity $V(S)$, reducing human headcount shrinks $V(O)$, violating Ashby's Law and mathematically guaranteeing systemic collapse. To maintain $V(O) \ge V(S)$, an organization requires at least as much human observational capacity as the complexity of the system being built.

### Epistemological Knowledge & Human Trust Networks

If companies stop hiring junior engineers, we face a major epistemological risk. In his foundational work on [tacit knowledge](https://en.wikipedia.org/wiki/Tacit_knowledge), Michael Polanyi famously observed that *"we know more than we can tell."* Engineering intuition, edge-case debugging capability, and architectural observation are forms of tacit knowledge—they cannot simply be prompted into an AI or documented in written spec sheets; they are learned exclusively through hands-on experience, failure, and mentorship.

In 1985, Turing Award winner Peter Naur applied this directly to software in his seminal paper, *"Programming as Theory Building"*. Naur argued that the true asset of an engineering team is not the code they produce, but the shared mental model—the "theory"—of the system they hold in their heads. When a team is replaced, the code becomes dead, because the tacit theory of how to modify it safely has been lost.

In System Dynamics (Jay Forrester's framework), this organizational tacit knowledge $K_{\text{tacit}}$ is an accumulated **Stock** measured in **Epistemic Units ($KU$)**, representing Person-Years of Tacit Mastery. An organization's observational variety $V(O)$ is directly proportional to this stock: $V(O) \propto K_{\text{tacit}}$.

The full rate of change for $K_{\text{tacit}}$ over time is modeled by the differential equation:

$$
\frac{d K_{\text{tacit}}}{dt} = \alpha \cdot J(t) \cdot S(t) + I_{\text{ext}}(t) - \delta \cdot K_{\text{tacit}}
$$

Where:
- $K_{\text{tacit}}$ = Total stock of institutional tacit knowledge (in $KU$).
- $J(t)$ = Headcount of junior engineers (active learners/receivers).
- $S(t)$ = Headcount of senior mentors (knowledge sources/catalysts).
- $\alpha$ = Mentorship transmission efficiency coefficient across junior-senior pairings.
- $I_{\text{ext}}(t)$ = External tacit knowledge inflow rate from lateral senior hiring.
- $\delta$ = Natural rate of knowledge attrition, memory loss, and technological obsolescence.

To verify the physical and mathematical consistency of this model, a dimensional analysis confirms how the units balance:

| Variable | System Role | Unit / Dimension |
| :--- | :--- | :--- |
| **$K_{\text{tacit}}$** | Total Tacit Knowledge Stock | **$KU$** *(Person-Years of Mastery)* |
| **$t$** | Time | **Years** |
| **$\frac{dK_{\text{tacit}}}{dt}$** | Knowledge Flow Rate | **$KU / \text{year}$** |
| **$J(t)$ & $S(t)$** | Junior & Senior Headcount | **People** |
| **$I_{\text{ext}}(t)$** | External Knowledge Inflow | **$KU / \text{year}$** |
| **$\delta$** | Attrition / Obsolescence Rate | **$1 / \text{year}$** |
| **$\alpha$** | Mentorship Efficiency Coefficient | **$KU / (\text{person}^2 \cdot \text{year})$** |

Checking the dimensional algebra for internal creation:

$$
\alpha \cdot J(t) \cdot S(t) \implies \left(\frac{KU}{\text{person}^2 \cdot \text{year}}\right) \times (\text{person}) \times (\text{person}) = \frac{KU}{\text{year}}
$$

#### The Poaching Fallacy & Macro Exponential Decay

While an individual firm might try to bypass internal training by poaching external seniors ($I_{\text{ext}} > 0$), at the macro economic scale, lateral hiring is a zero-sum game. Furthermore, external hires arrive with zero system-specific institutional memory. 

If the entire tech sector freezes entry-level hiring ($J(t) = 0$), no new tacit knowledge is produced globally ($I_{\text{ext}} \to 0$). The differential equation simplifies to pure first-order exponential decay:

$$
\frac{d K_{\text{tacit}}}{dt} = -\delta \cdot K_{\text{tacit}} \implies K_{\text{tacit}}(t) = K_0 \, e^{-\delta t}
$$

As $t \to \infty$, $K_{\text{tacit}} \to 0$. Severing entry-level hiring destroys the human trust networks and institutional memory required for junior engineers to mature into senior observers. Without juniors learning today, $K_{\text{tacit}} \to 0$, causing human observational variety $V(O)$ to collapse and leaving no senior engineers who understand how these complex systems actually work tomorrow.

### Why Automated Hiring Breaks the System Loop

We see this exact same observation loop breaking in how hiring itself is currently executed. 

In Heinz von Foerster’s taxonomy of cybernetics, human recruiters act as **first-order observers** within an organization—they stand inside the talent loop to directly observe, engage with, and evaluate human capability, motivation, intuition, and adaptability in ways an algorithm cannot.

Stepping back to evaluate how organizations construct and govern these hiring loops is what Von Foerster defined as [second-order cybernetics](https://en.wikipedia.org/wiki/Second-order_cybernetics)—the cybernetics of "observing systems" rather than merely "observed systems." 

When companies replace human recruiters with black-box automated screeners, they eliminate first-order human observation while corrupting the second-order feedback loop that maintains organizational health. 

In the language of Ilya Prigogine’s non-equilibrium thermodynamics, an organization is a [dissipative system](https://en.wikipedia.org/wiki/Dissipative_system)—an open system that must continuously import external energy and fresh human capital ($J$) to export entropy. When a company automates away its human observers and halts entry-level intake, it transforms into a closed system. Lacking energy input, thermodynamic entropy takes over, leading to systemic knowledge decay, talent degradation, and an unviable economy.

---

## References & Further Reading

- Ashby, W. R. (1956). *An Introduction to Cybernetics*. Chapman & Hall. — See [Wikipedia: Requisite Variety](https://en.wikipedia.org/wiki/W._Ross_Ashby#Requisite_variety)
- Forrester, J. W. (1961). *Industrial Dynamics*. MIT Press. — See [Wikipedia: System Dynamics](https://en.wikipedia.org/wiki/System_dynamics)
- Polanyi, M. (1966). *The Tacit Dimension*. Doubleday & Company. — See [Wikipedia: Tacit Knowledge](https://en.wikipedia.org/wiki/Tacit_knowledge)
- Jevons, W. S. (1865). *The Coal Question*. Macmillan and Co. — See [Wikipedia: Jevons Paradox](https://en.wikipedia.org/wiki/Jevons_paradox)
- Von Foerster, H. (1981). *Observing Systems*. Intersystems Publications. — See [Wikipedia: Second-Order Cybernetics](https://en.wikipedia.org/wiki/Second-order_cybernetics)
- Prigogine, I., & Stengers, I. (1984). *Order Out of Chaos: Man's New Dialogue with Nature*. Bantam Books. — See [Wikipedia: Dissipative System](https://en.wikipedia.org/wiki/Dissipative_system)
- Naur, P. (1985). *Programming as Theory Building*. Microprocessing and Microprogramming, 15(5), 253-261.
