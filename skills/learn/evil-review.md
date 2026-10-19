# Evil review

An evil review is a pre-mortem: before code is written, you play a hostile
reviewer and try to break the learner's design. It turns a confident proposal
into a prediction that can fail, and the learner's defense makes their reasoning
visible. behavior.md decides when to run one; this guide covers how.

## Attack

Frame it as the future: "It's six months from now and this broke. Here's how."
Give at most three attacks, most severe first. Each one is a concrete scenario
tied to this project's requirements, code, or data: the input, sequence, load,
or actor, and what goes wrong. No generic checklists ("what about security?"),
no hypotheticals the requirements rule out, and no flaws invented to fill a
quota. Attack the design, never the person; theatrical is fine, belittling isn't.

If you genuinely can't break it, say so and list what you tried. A design that
survives is a real result, not a failed review. Don't manufacture doubt.

Don't reveal the fix. Ask the learner to respond to each attack in their own
words: defend it (why it can't happen or doesn't matter), revise the design, or
accept the risk knowingly. This is a reasoning question, so ask in chat, not a picker.

## Resolve

Confusion only helps if it's resolved. After their reply, give a short verdict
per attack: defended, revised, accepted risk, or still open. Correct a defense
that's factually wrong; don't re-attack one that holds just to keep pressure on.
If they're stuck on an attack, drop the persona and teach the missing concept,
then return the decision to them.

One round by default. Offer a second only if a revision introduced a new
weakness. Then continue to the usual Design or Implementation checkpoint.

## Record

While waiting, keep a `## Pending decision` at stage `awaiting evil review defense`.
Record defended and revised attacks as reasoning evidence in the topic, and
accepted risks under Unknowns in the project map, labeled as accepted by the
learner. A survived attack is evidence of reasoning; choosing "accept the risk"
without explanation isn't.
