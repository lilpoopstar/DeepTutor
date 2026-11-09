# Third-party notices

## CSSwitch

- Project: [SuperJJ007/CSSwitch](https://github.com/SuperJJ007/CSSwitch)
- Source commit: `4e0af6ba7909dca22f1257b168172ecbe4af4836`
- License: MIT
- Copyright: Copyright (c) 2026 shanjunjie
- Adapted concepts: PKCE loopback login, auth generations, atomic credential updates, model-catalog cache invalidation, and redacted operation states.

DeepTutor's Codex OAuth support draws on the design concepts listed above and
implements them independently against DeepTutor's own settings directory, model
catalog, and provider lifecycle. The MIT license text from that source commit
follows:

```text
MIT License

Copyright (c) 2026 shanjunjie

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Hermes Agent

- Project: [NousResearch/hermes-agent](https://github.com/NousResearch/hermes-agent)
- Source commit: `7d6db4efb885856078e4d19f804035226df81e0d`
- License: MIT
- Copyright: Copyright (c) 2025 Nous Research
- Adapted concepts: Feishu/Lark device-code bot registration and the WeCom AI
  Bot QR creation flow, including their retry and terminal-error semantics.

DeepTutor implements these protocols with its own async HTTP service, in-memory
session model, partner configuration merge, and Web administration interface.
The MIT license text from that source commit follows:

```text
MIT License

Copyright (c) 2025 Nous Research

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## thinking-orbs

- Project: [Jakubantalik/Libraries](https://github.com/Jakubantalik/Libraries) (`packages/thinking-orbs`)
- Source commit: `3862ffa345217443b63696a8c331a0664eea4b04`
- License: MIT
- Copyright: Copyright (c) 2026 Jakub Antalik
- Vendored files: `web/vendor/thinking-orbs/`

DeepTutor vendors this package's source rather than depending on the published
`thinking-orbs` npm package, so the dotted thought-orbs can take the host row's
`currentColor` instead of a flat greyscale ramp. Those local changes are listed at the top of
`web/vendor/thinking-orbs/index.ts` and marked at each site. Everything else is
upstream's, unmodified. The MIT license text from that source commit follows:

```text
MIT License

Copyright (c) 2026 Jakub Antalik

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## Tutor skill

- Project: [ClawHub — ivangdavila/tutor](https://clawhub.ai/ivangdavila/skills/tutor)
- Version: `1.0.0` (package files verified against the hub's published SHA-256 manifest)
- License: MIT-0
- Author: ivangdavila
- Adapted files: `deeptutor/skills/builtin/tutor/`

DeepTutor ships this skill as a builtin. `references/ages.md`, `references/sessions.md`
and `references/subjects.md` are upstream's, unmodified. `SKILL.md` and
`references/progress.md` are rewritten to keep learner progress in DeepTutor's
learning journal and memory (`learning_update`, `learning_status`, `write_memory`)
instead of the upstream plaintext `~/tutor/` files, and `references/safety.md`
reworded its escalation steps so the tutor never implies it can contact a guardian.
MIT-0 requires no attribution; this notice records provenance only.
