# Game Interaction Verification

A lightweight skill for a single-user AI-agent workflow that checks game-effect interactions against legal, time-ordered game states.

## When to use

Use this skill when deciding whether multiple game rules or effects can legally interact to produce a stated outcome.

It verifies player roles, whose turn it is, target eligibility, timing windows, effect duration, and the sequence of state changes before declaring an interaction possible or impossible.

## Responsibility boundary

This skill validates concrete interactions from existing rules and effect texts. `repo-first-game-digitization` owns game-rule and design canons. Testing skills own executable test implementation, and review skills own their review workflows.

## Installation

Place `SKILL.md` in a `game-interaction-verification` directory under the target agent's supported skills directory. No runtime dependencies or setup files are required.

In a repository that maintains its own rules, give the agent access to the applicable canonical rules and effect texts. The skill derives results from those sources rather than carrying game-specific rulings.
