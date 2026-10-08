---
name: game-interaction-verification
description: Verify whether multiple game rules or effects can interact by tracing player roles, turn ownership, legal timing, targets, duration, and reachable state transitions.
---

# Game Interaction Verification

Use this skill when deciding whether multiple game rules or effects can legally interact to produce a stated outcome.

## Establish authoritative inputs

Read the applicable rules and exact effect texts before deriving a result. Use the repository's adopted rule and card sources when they exist. Identify the source for each material condition; distinguish stated rules from assumptions. Treat an unresolved material rule or missing effect text as an unresolved conclusion.

## Bind the players and effects

Assign stable identifiers to the relevant players (A, B, C, etc.). For each effect, identify its user or trigger source, its controller where relevant, the turn player, the objects it can affect, its activation or trigger timing, its resolution, and its expiration.

Interpret words such as "you", "your", and "opponent" relative to the appropriate effect or game rule, rather than to the player described first. Distinguish who uses an effect from who controls a card and whose turn is in progress. Distinguish effects that players use from effects that trigger automatically.

## Cover relevant role assignments

For two-player games, start by crossing who uses or controls the effect (A or B) with whose turn it is (A or B). Examine the resulting four role/turn cases when all are relevant, including effects used in response during the other player's turn. For games with more players, extend these role and turn assignments to the players relevant to the interaction.

For interactions involving more than one effect, also vary the assignments and ordering that can change their compatibility. Consolidate cases only when the rules establish that they are equivalent, or when a case is demonstrably illegal; record the reason.

## Trace legal states in time

For each distinct case:

1. Establish a reachable starting state with the necessary cards, resources, and timing.
2. List a legal sequence of actions, triggers, responses, and timing windows leading to the proposed interaction.
3. At each event, check the acting player, prerequisites, source and target eligibility, and the current game state against the governing text.
4. Resolve effects in their required order. Carry forward state changes and track each continuing effect until its stated expiration.
5. At the point where the effects are claimed to interact, check that their relevant conditions are simultaneously satisfied. For continuing effects, verify their effective intervals overlap at that point; for sequential effects, verify that the required resulting state persists.

Use the state at the actual time of each decision. Re-evaluate derived values after earlier changes rather than relying on the initial values.

## Verify the result

For a claim that an interaction is possible, exhibit a complete legal sequence that reaches it. For a claim that it is impossible, rule out each relevant role, turn, and ordering case with the specific unmet condition. When evidence cannot establish either conclusion, state what remains unresolved.

Recheck the proposed sequence against each effect's authoritative text independently of the initial conclusion, especially relative player words, off-turn permissions, target ownership, and expiration boundaries. When an executable game engine is available, use it for additional verification while keeping authoritative rules as the basis for correctness.

## Report

Give the conclusion, a concrete role assignment and event sequence supporting it, and the decisive rule sources or unresolved assumptions. Use a compact case matrix or timeline when several cases matter; keep straightforward cases concise.

This skill owns validation of concrete game-effect interactions. Canon creation and upkeep belong to the surrounding game-digitization workflow; test implementation and PR review belong to their respective workflows.
