# post-training-receipts

Small-scale reproductions of post-training and agent-RL claims, with logs
and negative results. A failed reproduction is recorded the same way a
successful one is — the point is the receipt, not a win rate.

## Entry format

Every reproduction lives in its own directory:

```
entries/<date>-<slug>/
  claim.md        # the claim being reproduced, with a source citation
  plan.json        # the reproduction plan: steps, budget, success criteria
  script.py        # the code that ran
  log.txt          # raw output from the run
  result.json      # measured outcome + verdict (confirmed/refuted/inconclusive)
  evidence.json    # every number in result.json traced to a source or a log line
```

`claim.md` states what is being tested and cites where the claim comes
from. `plan.json` is written before the run, not after. `result.json`
always carries a verdict; `evidence.json` is what makes that verdict
checkable rather than asserted.

## License

Code in this repository (scripts, plans, tooling) is MIT-licensed — see
`LICENSE`. Each entry's `claim.md` cites the sources for the claim it
reproduces; those sources keep their own license and are not covered by
this repository's MIT grant.
