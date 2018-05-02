- Feature Name: Unicode Operators
- Start Date: 2018-05-01
- RFC PR: (leave this empty)
- Rust Issue: (leave this empty)

# Summary
[summary]: #summary

Allow the use of Unicode Operators, specifically and primarily Unicode Mathematical Symbols and Arrow Symbols, as Trait-Driven Operators in Rust.

# Motivation
[motivation]: #motivation

Why are we doing this? 

There have been a number of discussions, Pre-RFC's, and RFC's proposing additional operators (primarily mathematical, set theoretic, type-theory, or functional programming related) constructed from various, somewhat arbitrary, combinations of various ASCII punctuation/non-alpha-numeric characters (``!@#$%`^&*()_-+={[}]|\\:;"'<,>.?/~``). This seems to indicate a clear desire by a not insignificant portion of the Rust community to extend the available operators that the Rust compiler supports through Trait Implementations. The problem with most of the proposals is that the proposed operators, as combinations of ASCII punctuation, tend to lead to less readable code and so the proposals are more often than not rejected by the community due to the fact that the apparent cost to the readability of Rust is far greater than any benefit derived from adding the operator to the language.

This RFC makes the claim that if Rust supported Unicode Mathematical Symbols (and other similar Unicode Code Blocks) as operators (backed by Traits and Trait Implementations) would, provided there is sufficient ecosystem support and that the vast majority of editors and IDE's used by the Rust community have sufficient support for the entry and display of Unicode Mathematical (and similar) symbols, allow for extremely readable, and not overly difficult to write, code for mathematically, set theoretic, type-theory, and functional programming related operators.

What use cases does it support? 

What is the expected outcome?

# Guide-level explanation
[guide-level-explanation]: #guide-level-explanation

Explain the proposal as if it was already included in the language and you were teaching it to another Rust programmer. That generally means:

- Introducing new named concepts.
- Explaining the feature largely in terms of examples.
- Explaining how Rust programmers should *think* about the feature, and how it should impact the way they use Rust. It should explain the impact as concretely as possible.
- If applicable, provide sample error messages, deprecation warnings, or migration guidance.
- If applicable, describe the differences between teaching this to existing Rust programmers and new Rust programmers.

For implementation-oriented RFCs (e.g. for compiler internals), this section should focus on how compiler contributors should think about the change, and give examples of its concrete impact. For policy RFCs, this section should provide an example-driven introduction to the policy, and explain its impact in concrete terms.

# Reference-level explanation
[reference-level-explanation]: #reference-level-explanation

This is the technical portion of the RFC. Explain the design in sufficient detail that:

- Its interaction with other features is clear.
- It is reasonably clear how the feature would be implemented.
- Corner cases are dissected by example.

The section should return to the examples given in the previous section, and explain more fully how the detailed proposal makes those examples work.

# Drawbacks
[drawbacks]: #drawbacks

Why should we *not* do this?

# Rationale and alternatives
[alternatives]: #alternatives

- Why is this design the best in the space of possible designs?
- What other designs have been considered and what is the rationale for not choosing them?
- What is the impact of not doing this?

# Prior art
[prior-art]: #prior-art

Discuss prior art, both the good and the bad, in relation to this proposal.
A few examples of what this can include are:

- For language, library, cargo, tools, and compiler proposals: Does this feature exist in other programming languages and what experience have their community had?
- For community proposals: Is this done by some other community and what were their experiences with it?
- For other teams: What lessons can we learn from what other communities have done here?
- Papers: Are there any published papers or great posts that discuss this? If you have some relevant papers to refer to, this can serve as a more detailed theoretical background.

This section is intended to encourage you as an author to think about the lessons from other languages, provide readers of your RFC with a fuller picture.
If there is no prior art, that is fine - your ideas are interesting to us whether they are brand new or if it is an adaptation from other languages.

Note that while precedent set by other languages is some motivation, it does not on its own motivate an RFC.
Please also take into consideration that rust sometimes intentionally diverges from common language features.

# Unresolved questions
[unresolved]: #unresolved-questions

- What parts of the design do you expect to resolve through the RFC process before this gets merged?
- What parts of the design do you expect to resolve through the implementation of this feature before stabilization?
- What related issues do you consider out of scope for this RFC that could be addressed in the future independently of the solution that comes out of this RFC?
