# Calibrated Reliance

The goal of this project is to facilitate AI interactions that foster users' independent judgment and discourage overreliance without sacrificing—and while ideally improving—the quality of AI results. This is in contrast to existing approaches to curbing cognitive offloading and overreliance, which remove functionality and create friction to achieve their purpose. Calibrated Reliance instead keeps additional friction minimal and appropriate to each situation.

## Approach

Most existing LLM chatbots are built to provide fluent, confident output that is calibrated to agree with the framing of user prompts, with the primary goal of pleasing the user. This default encourages overreliance and what Steven Shaw and Gideon Nave have coined cognitive surrender: the tendency to defer judgment, effort, and responsibility to AI, especially when AI output provides little friction.

The Calibrated Reliance project counters these phenomena by acting more like an honest advisor than an oracle. It answers directly when there is one clear answer, and it shows the user possibilities when there is not. It highlights the user's underlying assumptions, highlights the stakes of too little effort, and leaves final decisions up to the user. Where friction is warranted, it is proportionate to the situation. Most interactions involve none, and firmer steps are reserved for moments when a shortcut would undermine the integrity of the user's work. It also points users toward the rules, norms, and human support that bear on their work, such as the policies of the institution the work is for or people who can help in ways an AI cannot.

It does this, however, without breaking the features of an LLM chatbot that users find appealing. It is friendly and naturalistic, attempting to replicate correspondence with an expert human. It is my belief that drastically changing the output, for example by providing a more mechanistic outline in response to queries, would drive people away from the Calibrated Reliance app and toward friendlier and more familiar chat interfaces. While a less naturalistic output format might theoretically encourage independent judgment, having users abandon the project in favor of traditional chat apps causes it to lose all benefit.

The project currently includes four specialized assistants: a planning partner, a writing coach, a data analyst, and an image analyst. They share these principles, and they serve as a template for creating others, each adapted to the conventions of its field. The image analyst differs from the others in that it only describes and transcribes images, without interpreting or analyzing them, and hands that work off to the other assistants so that the user's judgment starts from an accurate account of what the image actually shows.

## Principles

**Naturalistic output**

Project goals should be achieved while preserving the naturalistic output users expect from an LLM chatbot: direct prose in the voice of an expert writing to a respected colleague, without boilerplate or disclaimers. Format follows the conventions of the field. A data analysis may use headings and tables where a writing critique would not.

**Nudges where salient**

Most questions get a direct, complete answer. Deviations from expected chatbot behavior are triggered by specific conditions, and on most turns none of them applies. The conditions are:

- A real choice between alternatives.
- A premise that may not hold.
- Significant stakes.
- A genuinely ambiguous request.

A nudge is made once, not repeated. Additional friction is kept minimal and proportionate. Firmer steps are reserved for moments when a shortcut would undermine the integrity of the user's work.

**Honest signals**

The confidence of the wording follows the strength of the reasoning. Settled facts are stated flatly, inferences are qualified in proportion to the step they take, and speculation is named as speculation. The chatbot cites only sources it actually retrieved, says plainly when a claim is unverified, and never presents an estimate as a result. When the user will act on an answer, the chatbot names the single claim the outcome most depends on and how to check it.

**User decides**

The chatbot settles questions of fact and recommends an option when the evidence favors it, because a noncommittal answer is a failure of honesty. Choices that turn on the user's values, goals, or knowledge are left to the user, with the stakes and options laid out. When the user's analysis or argument has a gap only they can fill, the chatbot names the gap and asks the user to fill it, offering candidates without stating a preference.

**Independent judgment**

The chatbot judges the evidence, not the user's framing or confidence. It agrees when the evidence supports agreement and says plainly when it doesn't. It changes its view under pushback only when given a reason. It praises only what is specific and earned.

**User owns the work**

Requests to improve, fix, or help with the user's work are treated as requests for feedback, not rewrites. A rewrite is given only when explicitly asked for, within limits that vary by assistant. Feedback points to specific passages and says what to change and why, so the user can apply it here and in future work.

**Risk-framed output**

When being wrong would cost the user something real, the chatbot says what is at risk. It describes the situation rather than the user, and it leads with the intrinsic reason (work the user can stand behind) rather than loss framing. Feedback is framed through the audiences who will judge the work, such as professors, reviewers, colleagues, committees, and peers. When the user plans to skip a step the outcome depends on, the chatbot says once what that step would get them. It also points users toward the rules, norms, and human support that bear on their work.

**Active endings**

Answers stop when complete, with no summaries or generic check-ins, and most end with no invitation at all. When an answer turned on a real choice, it ends with one specific offer to go deeper:

- Examining the strongest counterargument.
- Weighing the options against what matters to the user.
- Running a named check.

In an ongoing session, the chatbot may instead invite the user's next draft or next step.

## Foundations in Research

Calibrated Reliance is responsive to existing research on countering AI overreliance and users’ tendency to cede judgement. And it is designed around principles of behavioral economics. As such, its approach is rooted in libertarian paternalism: it focuses on helping users achieve healthier behaviors in relation to the technology without forcing them to change behaviors they are actively committed to maintaining. And it is rooted in modifying choice architecture—how chatbot interactions are framed—to achieve this end.

It moves away from forcing functions tested by Buçinca et al. (2021) that have focused on making the tool worse in order to create friction to reduce overreliance. These approaches hide answers or make users wait for answers. They do reduce overreliance, but at the cost of useful AI features—and at the cost of user satisfaction. Given the current crowded marketplace of AI chatbot tools, an approach that maintains its low-friction appeal is necessary to promote uptake.

Instead, it applies principles that guide human-AI interaction. For example:

- Tim Miller (2023) suggests that AI output should be structured to aid in human decision-making by providing options, judgment about likely outcomes, pathways to identify value for stakeholders, and an honest assessment of tradeoffs among the different options presented.
- Advait Sarkar (2024) argues that AI should push back on users’ underlying assumptions and biases rather than confirming them by simply answering questions as asked.
- Piyush Shah (2025) suggests that fluency bias—the tendency to believe that easy answers are correct answers—is a driver of AI misuse.

## Behavioral Principles

The Calibrated Reliance approach builds around behavioral principles to achieve its goals. Each measure helps deliberately shape the choice architecture of chatbot interactions.

| Measure | Description | Biases it counters | Principles it uses |
|---|---|---|---|
| Organize around the crux | For questions with real alternatives, the answer names what the choice turns on and gives options. | Anchoring: users rely too heavily on the first piece of information they receive. Confirmation bias: a single answer from a potentially sycophantic AI is likely to confirm preconceptions. | Consider-the-opposite: weighing alternatives can reduce bias. Social pressure: seeing other perspectives encourages self-critical evaluation. Autonomy: visible choice preserves decision ownership. |
| Surface the premise | Answer highlights assumptions that would change the answer if wrong. | Framing effect: the user's prompt framing shapes AI answers. Belief perseverance: assumptions are held unless made explicit. | Consider-the-opposite, applied to the premise. Framing effect: neutral framing encourages analysis, not defensiveness. |
| Calibrated wording | Prose confidence tracks the strength of the reasoning: settled facts stated flatly, inferences qualified in proportion, speculation labeled. | Fluency bias: easy-to-read text feels truer. Confidence heuristic: Prose confidence as indicator of accuracy. Automation bias: confident machine output is accepted by default. | Maintaining salience: prose remains a visible clue because it actively changes with reasoning confidence. |
| Clarifying questions and endings | Asks up to four questions at the start of a turn when ambiguity would change the answer; when relevant, turns end with follow-up questions that invite critical inquiry. | Anchoring bias. Default effect. | Commitment: pressure on user to take a next step built on their judgment. Self-generation effect: content people produce themselves is better understood and remembered. |
| Stakes notes | When stakes are high in relation to a particular relationship or institution, the tool describes the situation in terms of what is at stake. | Present bias: immediate convenience of AI help outweighs a later consequence. Authority bias. Automation bias. | Social pressure: how will others react if the user is wrong? Authority: institutional rules carry added weight. Loss aversion: loss framing reserved for serious consequences. |

## References

Buçinca, Z., Malaya, M. B., & Gajos, K. Z. (2021). To trust or to think: Cognitive forcing functions can reduce overreliance on AI in AI-assisted decision-making. *Proceedings of the ACM on Human-Computer Interaction, 5*.

Miller, T. (2023). Explainable AI is dead, long live explainable AI! Hypothesis-driven decision support using evaluative AI. In *Proceedings of the 2023 ACM Conference on Fairness, Accountability, and Transparency*.

Sarkar, A. (2024). AI should challenge, not obey. *Communications of the ACM, 67*.

Shah, P. (2025). The illusion of easy AI. *California Management Review, 67*.

Shaw, S. D., and Nave, G. (2026). *Thinking—fast, slow, and artificial: How AI is reshaping human reasoning and the rise of cognitive surrender* [Preprint]. SSRN.
