Fourth proof round, 2026-09-04, pull request cinatra#3197 (issue #3002), branch fix/3002-completion-card-transcript-pointer at its live head, on a dev boot per the standing ruling, graded against the ratified drawing at design main. Pictures by permalink from the proofs repository.

**The run's own page, completed, light**

![The run's own page, completed, light](PLACEHOLDER/r4-run-page-completion-card-light.png?raw=true)

[full-size file](PLACEHOLDER/r4-run-page-completion-card-light.png)

**The run's own page, completed, dark**

![The run's own page, completed, dark](PLACEHOLDER/r4-run-page-completion-card-dark.png?raw=true)

[full-size file](PLACEHOLDER/r4-run-page-completion-card-dark.png)

**The chat mount, completed, light**

![The chat mount, completed, light](PLACEHOLDER/r4-chat-mount-completion-card-light.png?raw=true)

[full-size file](PLACEHOLDER/r4-chat-mount-completion-card-light.png)

**The chat mount, completed, dark**

![The chat mount, completed, dark](PLACEHOLDER/r4-chat-mount-completion-card-dark.png?raw=true)

[full-size file](PLACEHOLDER/r4-chat-mount-completion-card-dark.png)

**The run's own page, after reload, light**

![The run's own page, after reload, light](PLACEHOLDER/r4-run-page-after-reload-light.png?raw=true)

[full-size file](PLACEHOLDER/r4-run-page-after-reload-light.png)

**The run's own page, after reload, dark**

![The run's own page, after reload, dark](PLACEHOLDER/r4-run-page-after-reload-dark.png?raw=true)

[full-size file](PLACEHOLDER/r4-run-page-after-reload-dark.png)

**The chat mount, after reload, light**

![The chat mount, after reload, light](PLACEHOLDER/r4-chat-mount-after-reload-light.png?raw=true)

[full-size file](PLACEHOLDER/r4-chat-mount-after-reload-light.png)

**The chat mount, after reload, dark**

![The chat mount, after reload, dark](PLACEHOLDER/r4-chat-mount-after-reload-dark.png?raw=true)

[full-size file](PLACEHOLDER/r4-chat-mount-after-reload-dark.png)

| requires | shows | verdict |
|---|---|---|
| Run page: the card carries the ratified title, the sentence verbatim, the Start new run control, the completed pill in the dot form, the Final response row beneath | title, sentence, control and pill all present and correct in both palettes; the card renders as one box rather than the drawing's nested pair, the header row and its title are absent, and the pill sits outside the card | BEHAVIOUR PASS, DRAWN SURFACE FAIL |
| Chat mount at the live completion instant: the card's sentence must agree with what is rendered beneath it | the card reads the fallback sentence while the run's own output already stands beneath it in the same card, in both palettes | BEHAVIOUR FAIL |
| Chat mount, Start new run: a host never drops an affordance the card's own section draws | the control is absent on all four chat-mount frames, before and after reload | DRAWN SURFACE FAIL |
| After a reload of each surface, the card and the transcript row still stand | both surfaces hold the card and the row after reload; the chat mount's sentence resolves to the ratified wording once reloaded | BEHAVIOUR PASS |

Own items: run page 12-13 of 19-20 per frame; chat mount 9-12 of 17-18 per frame. Departures outside this issue's own cells are recorded in the round's comment with their numbers.
