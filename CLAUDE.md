# Game Developer Lifecycle

Follow this lifecycle for all development work:

1. **Spec Phase**: Write `docs/spec.md`. DO NOT code yet.
2. **Roadmap Phase**: Break spec into `docs/roadmap.md` with 5-7 distinct features.
3. **Execution**: Implement one feature, run tests, and then `git commit`.
4. **Verification**: Use the `computer-use` tool to verify the game loop visually.
5. **Approval**: Ask for permission ONLY after the `git commit` is successful.

> **Always commit changes as you go.** Every meaningful change — including updates to `CLAUDE.md` itself — should be committed immediately.

# Dev Server

When the user wants to play the game, serve it at **http://localhost:3000** using:
```
python3 -m http.server 3000
```
Run from `/home/claude/workspace`. Do this automatically without being asked.
