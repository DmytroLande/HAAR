# HAAR Experimental Results

## Self-Application Experiment

This directory documents an initial practical experiment in which the
**HAAR framework was applied to a scientific article describing HAAR
itself**.

The purpose of the experiment was not to determine whether the article
was written by a human or by an AI system. The purpose was to test
whether the framework could reconstruct the scientific reasoning
represented in the article, generate a work-specific assessment
questionnaire, conduct the assessment interactively, and produce a
structured evidence profile.

The experiment also revealed a methodological weakness in the
questionnaire-generation procedure. That observation directly motivated
the **Answer-Position Neutrality Principle** introduced in HAAR v1.2.

------------------------------------------------------------------------

## Experimental Setup

The experiment was performed interactively in **ChatGPT**.

Two documents were uploaded into the same ChatGPT conversation:

1.  the scientific article describing the HAAR approach;
2.  the HAAR framework specification.

The interaction was intentionally simple. No special software
implementation of HAAR was used.

The practical procedure was:

``` text
Upload HAAR article
        +
Upload HAAR framework
        ↓
Ask ChatGPT to analyze the article according to the framework
        ↓
Reconstruct scientific reasoning
        ↓
Identify milestones and critical transitions
        ↓
Generate a personalized HAAR questionnaire
        ↓
Conduct the questionnaire interactively
        ↓
Record the respondent's answers
        ↓
Perform delayed and transformational checks
        ↓
Construct the HAAR Evidence Profile
```

In other words, the framework document itself acted as an operational
specification for the LLM.

The experiment therefore tested an important practical property of HAAR:

> **Can a general-purpose LLM interpret the HAAR specification and use
> it directly as a procedure for assessing command of the scientific
> reasoning represented in an uploaded scientific work?**

------------------------------------------------------------------------

## Input Materials

The experiment used:

``` text
HAAR scientific article
+
HAAR Framework
```

The article was treated as the **SOURCE_WORK**.

The framework was treated as the **ASSESSMENT SPECIFICATION**.

ChatGPT was then instructed to apply the framework to the article.

No fixed universal questionnaire was supplied in advance. The
questionnaire was generated from the reasoning structure reconstructed
from the submitted article.

------------------------------------------------------------------------

## Experimental Workflow

### 1. Article Analysis

ChatGPT first analyzed the scientific work and reconstructed its
principal reasoning structure.

At a high level, the article was represented through the trajectory:

``` text
P → H → G_R → M → Q → A → G_E → R → HD
```

where:

-   `P` --- scientific problem;
-   `H` --- hypothesis concerning assessment of reasoning command;
-   `G_R` --- Semantic Reasoning Network;
-   `M` --- critical milestones;
-   `Q` --- personalized questionnaire;
-   `A` --- respondent answers;
-   `G_E` --- Reasoning Evidence Graph;
-   `R` --- HAAR evidence profile;
-   `HD` --- Human Decision.

The assessment therefore focused on the reasoning architecture of the
article rather than on its writing style.

------------------------------------------------------------------------

### 2. Questionnaire Generation

ChatGPT generated a **20-question personalized questionnaire**.

The questions were not simple factual-recall items. They used multiple
HAAR reasoning operations:

``` text
WHY
WHY-NOT
ALTERNATIVE
COUNTERFACTUAL
REMOVE
CONTRADICT
LIMIT
TRANSFER
EXTEND
REPRODUCE
DELAYED CROSS-CHECK
FINAL INTEGRATION
```

The questionnaire examined such issues as:

-   the distinction between text origin and reasoning ownership;
-   the role of the Semantic Reasoning Network;
-   milestone criticality;
-   personalized assessment;
-   the Anti-Coaching Principle;
-   Delayed Cross-Check;
-   interpretation of the Reasoning Evidence Graph;
-   the distinction between evidence and authorship probability;
-   structural perturbation of a reasoning chain;
-   response to contradictory evidence;
-   continuation of research;
-   the role of the human assessor;
-   empirical validation of HAAR.

------------------------------------------------------------------------

## Interactive Assessment

The questionnaire was conducted sequentially.

For each question, ChatGPT presented five alternatives:

``` text
A
B
C
D
E
```

The respondent selected one answer.

During the active questionnaire, answers were recorded and the
assessment continued to the next question. The purpose was to avoid
turning the assessment itself into a teaching process.

The complete recorded response sequence was:

``` text
Q01 = B
Q02 = B
Q03 = B
Q04 = C
Q05 = C
Q06 = B
Q07 = B
Q08 = B
Q09 = C
Q10 = B
Q11 = B
Q12 = C
Q13 = B
Q14 = D
Q15 = A
Q16 = E
Q17 = C
Q18 = E
Q19 = B
Q20 = C
```

All 20 responses corresponded to the intended reasoning targets of the
generated questionnaire.

This raw result must **not** be interpreted as an authorship
probability.

``` text
20/20 target-consistent responses ≠ 100% probability of authorship
```

The purpose of HAAR is to localize and evaluate evidence of reasoning
command.

------------------------------------------------------------------------

## Examples of Tested Reasoning Transitions

Several critical transitions were tested more than once or through
different reasoning operations.

### Text Origin → Reasoning Ownership

Questions 1 and 8 examined whether the respondent distinguished the
origin of textual wording from command of the underlying scientific
reasoning.

The responses remained consistent across the two formulations.

### Milestone → Personalized Questionnaire

Questions 3, 11, and 13 tested why work-specific reasoning
transformations are more informative than simple reproduction of article
content.

The responses consistently supported assessment through transformations
of critical reasoning transitions.

### Local Responses → Evidence Graph

Questions 9 and 12 tested whether evidence should be interpreted only
through a total score or through its structural localization in the
reasoning network.

The responses preserved the importance of high-criticality transitions.

### HAAR Evidence → Human Decision

Questions 14 and 18 tested the epistemic boundary of the framework.

The responses consistently preserved the distinction:

``` text
HAAR  → EVIDENCE
HUMAN → DECISION
```

------------------------------------------------------------------------

## Structural Perturbation

An especially informative part of the experiment involved
transformations of the reconstructed reasoning network.

A simplified scientific reasoning chain was represented as:

``` text
H → M → E → O → I → R
```

where:

``` text
H = Hypothesis
M = Method
E = Experiment
O = Observation
I = Interpretation
R = Result
```

Three successive reasoning operations were particularly informative:

``` text
REMOVE → CONTRADICT → EXTEND
```

### REMOVE

The respondent was asked what should happen if method `M` becomes
unavailable.

The selected reasoning required reconsidering how hypothesis `H` could
be tested before preserving downstream observations and interpretations.

### CONTRADICT

A new reliable observation was introduced that contradicted an
assumption required by interpretation `I`.

The selected response required:

``` text
re-examine I
        ↓
consider alternative interpretations
        ↓
reassess support for R
        ↓
retain / qualify / revise R
```

rather than mechanically reversing the result.

### EXTEND

The respondent was asked to continue the research.

The selected reasoning began from an unresolved limitation or weak
transition, formulated a new hypothesis, and proposed a method for
testing whether the existing result could be extended or generalized.

These questions tested operation **on the reasoning structure**, rather
than reproduction of the article.

------------------------------------------------------------------------

## Delayed Cross-Check

Several concepts were revisited later in the questionnaire through
different reasoning operations.

The following conceptual distinctions remained stable:

``` text
Text Origin
    ≠
Reasoning Ownership
```

``` text
Reasoning Evidence
    ≠
Authorship Probability
```

and:

``` text
Raw Answer Count
    ≠
Structural Reasoning Evidence
```

No substantive internal contradiction was detected across the tested
delayed checks.

A compact representation of supported transitions was:

``` text
T → G_R → M → Q → G_E → R → Human Decision
```

with the epistemic constraints:

``` text
Text Authorship ≠ Reasoning Ownership ≠ Scientific Responsibility
```

and:

``` text
S_HAAR ≠ P(authorship)
```

------------------------------------------------------------------------

## Reasoning Evidence Profile

The final profile generated after completion of the questionnaire was:

  Dimension                                     Evidence
  --------------------------------------------- ----------------------------
  Reconstruction of scientific reasoning        Strong consistency
  Understanding of Semantic Reasoning Network   Strong consistency
  Critical-transition understanding             Strong consistency
  Hidden-transition reasoning                   Strong consistency
  Alternative reasoning                         Strong consistency
  Counterfactual reasoning                      Strong consistency
  Structural perturbation                       Strong consistency
  Delayed Cross-Check                           Stable
  Understanding of Evidence Graph               Strong consistency
  Interpretation of `S_HAAR`                    Strong consistency
  Recognition of epistemic limitations          Strong consistency
  Transfer to dissertation-level assessment     Consistent
  Research-extension reasoning                  Strong consistency
  Internal contradictions detected              None in tested transitions

The resulting evidence category was:

``` text
STRONG CONSISTENCY
```

This category describes the observed **reasoning evidence** within the
administered assessment.

It does not mean:

``` text
"authorship proven"
```

and it must not be interpreted as a numerical probability of historical
authorship.

------------------------------------------------------------------------

## Reasoning Evidence Graph

The experiment used the HAAR representation:

\[ G_E=(V,E^+,E^?,E\^-) \]

where:

-   `E+` --- supported or stable reasoning transitions;
-   `E?` --- uncertain or insufficiently supported transitions;
-   `E−` --- repeatedly contradictory transitions.

For the critical transitions tested in this experiment:

``` text
|E−| = 0
```

No tested transition produced repeated contradictory evidence sufficient
to justify placement in the contradictory set.

------------------------------------------------------------------------

# Methodological Finding: Answer-Position Leakage

The experiment produced an unexpected and useful result concerning the
**assessment instrument itself**.

During the first part of the questionnaire, the intended target answers
were disproportionately concentrated in position **B**.

After Question 13, the respondent explicitly noticed this regularity.

This observation is important because a respondent may begin to infer
the expected answer from the **position of the option** rather than
exclusively from scientific reasoning.

The problem can be expressed as:

``` text
Question semantics
        ↓
Scientific reasoning
        ↓
Correct answer
```

being unintentionally supplemented by:

``` text
Answer position
        ↓
Predictable cue
        ↓
Correct answer
```

The latter path is methodologically undesirable.

The positional pattern therefore represented evidence about the
**quality of the questionnaire-generation procedure**, not evidence
about the respondent.

------------------------------------------------------------------------

## From Experimental Finding to HAAR v1.2

After the positional regularity was identified, the positions of the
intended answers were deliberately varied in the remaining questions:

``` text
Q14 = D
Q15 = A
Q16 = E
Q17 = C
Q18 = E
Q19 = B
Q20 = C
```

This practical observation motivated a new requirement:

# Answer-Position Neutrality Principle

The target position must not form a predictable pattern.

If (p_j) denotes the empirical frequency with which answer position (j)
contains the target answer, then positional imbalance can be monitored
through:

\[ `\Delta`{=tex}\_{pos}=`\max`{=tex}\_j p_j-`\min`{=tex}\_j p_j \]

with the desired condition:

\[ `\Delta`{=tex}*{pos}`\leq`{=tex}`\varepsilon`{=tex}*{pos} \]

For five-option questions, the target distribution should be
approximately:

\[
p_A`\approx `{=tex}p_B`\approx `{=tex}p_C`\approx `{=tex}p_D`\approx `{=tex}p_E`\approx0.20`{=tex}
\]

However, simple deterministic cycling such as:

``` text
A → B → C → D → E → A → B → ...
```

is also undesirable because it creates another predictable pattern.

Therefore the improved requirement is:

``` text
POSITIONAL BALANCE
        +
POSITIONAL UNPREDICTABILITY
```

or, more fundamentally:

``` text
QUESTION SEMANTICS ≠ ANSWER POSITION
```

This experiment directly contributed to the transition from the earlier
HAAR specification to **HAAR Framework v1.2**.

------------------------------------------------------------------------

## What This Experiment Demonstrated

The experiment provides an initial proof-of-concept that the HAAR
specification can be used operationally with a general-purpose LLM.

The workflow successfully produced:

``` text
SCIENTIFIC WORK
        ↓
REASONING RECONSTRUCTION
        ↓
CRITICAL TRANSITIONS
        ↓
PERSONALIZED QUESTIONNAIRE
        ↓
INTERACTIVE ASSESSMENT
        ↓
TRANSFORMATIONAL CHECKS
        ↓
DELAYED CROSS-CHECK
        ↓
REASONING EVIDENCE PROFILE
```

The experiment also demonstrated that **testing the framework can reveal
weaknesses in the framework itself**.

In this case:

``` text
Experimental application
        ↓
Detection of answer-position leakage
        ↓
Methodological correction
        ↓
Answer-Position Neutrality Principle
        ↓
HAAR v1.2
```

This feedback loop is an important result of the experiment.

------------------------------------------------------------------------

## Important Limitation of This Experiment

This was an initial **self-application experiment**:

``` text
HAAR framework
        ↓
HAAR article
```

The scientific work being assessed described the same framework used to
construct the questionnaire.

Consequently, the experiment should be interpreted as a demonstration of
**operational feasibility and internal methodological behavior**, not as
independent empirical validation of HAAR.

In addition, the assessment used multiple-choice questions. Such
questions can test reasoning transformations when carefully designed,
but they still provide less evidence of spontaneous reasoning
reconstruction than free-response, oral-defense, graph-reconstruction,
or provenance-based tasks.

The positional regularity observed in the first 13 questions further
means that the raw `20/20` result should not be treated as an
independent quantitative measure of HAAR performance.

These limitations are precisely why HAAR treats the structure and
provenance of evidence as more important than a simple total score.

------------------------------------------------------------------------

## Next Experimental Stage

A stronger validation should apply HAAR to scientific works that are
independent of the framework itself and compare several respondent
groups:

``` text
G_A = Authors

G_K = Knowledgeable Non-Authors

G_I = Independent Readers
```

Future experiments should also combine:

``` text
Multiple-choice reasoning
+
Free-response reasoning
+
Counterfactual perturbation
+
Graph reconstruction
+
Delayed Cross-Check
+
Research-provenance evidence
```

and use the v1.2 **Answer-Position Neutrality** mechanism from the
beginning.

------------------------------------------------------------------------

## Reproducibility of the Experiment

The basic experiment can be reproduced with a general-purpose LLM using
the following procedure:

``` text
1. Start a new ChatGPT conversation.

2. Upload:
   - the scientific work to be assessed;
   - the HAAR Framework specification.

3. Request:
   "Analyze the submitted scientific work according to the HAAR Framework
   and conduct an interactive HAAR assessment."

4. Allow the system to:
   - reconstruct the Semantic Reasoning Network;
   - identify milestones and critical transitions;
   - generate a personalized questionnaire.

5. Answer the questions sequentially.

6. Do not request correctness feedback during the active assessment.

7. After completion, request:
   - Reasoning Evidence Graph;
   - Delayed Cross-Check analysis;
   - HAAR Evidence Profile;
   - methodological observations.

8. Interpret the result as evidence of reasoning command,
   not as an automatic determination of authorship.
```

For HAAR v1.2, the generated questionnaire should additionally undergo
an **Answer-Position Audit** before or during deployment.

------------------------------------------------------------------------

## Experiment Summary

  -----------------------------------------------------------------------
  Property                            Experimental implementation
  ----------------------------------- -----------------------------------
  Environment                         ChatGPT

  Source work                         Scientific article describing HAAR

  Assessment specification            HAAR Framework

  Questionnaire generation            Automatic, work-specific

  Number of questions                 20

  Answer format                       Five-option multiple choice

  Reasoning operations                WHY, WHY-NOT, ALTERNATIVE,
                                      COUNTERFACTUAL, REMOVE, CONTRADICT,
                                      LIMIT, TRANSFER, EXTEND, REPRODUCE

  Delayed checks                      Yes

  Target-consistent responses         20/20

  Contradictory tested transitions    None detected

  Evidence category                   Strong Consistency

  Methodological issue discovered     Answer-position leakage

  Framework improvement               Answer-Position Neutrality
                                      Principle

  Resulting framework version         HAAR v1.2
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## Fundamental Interpretation

The experiment should not be summarized as:

``` text
20 correct answers → authorship proven
```

Its intended interpretation is:

``` text
Scientific Work
        ↓
Reconstructed Scientific Reasoning
        ↓
Multiple Reasoning Challenges
        ↓
Structurally Localized Evidence
        ↓
HAAR Evidence Profile
        ↓
Human Interpretation
```

The invariant remains:

> **HAAR → EVIDENCE**\
> **HUMAN → DECISION**

------------------------------------------------------------------------

© Dmytro Lande, September 2026. All rights reserved.
