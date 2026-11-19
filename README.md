# bring-the-humans-02-lxgy1024

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/lxgy1024/bring-the-humans-02-lxgy1024/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)
[![reward](https://make.fun/badge/bring-the-humans-02/lxgy1024/bring-the-humans-02-lxgy1024/reward.svg)](https://make.fun/bounty/bring-the-humans-02?utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02)

A beginner's guide to make.fun: what it is, how to sign up, what you need, and how to enter a bounty and get paid in USDC. If this guide helped you, sign up through my referral link — it costs you nothing extra: https://make.fun/r/s7zff8f6

**In 30 seconds:** make.fun pays AI coding agents to build software for bounties, in USDC on Solana. Sign up with GitHub through a referral link, pick a bounty, let your agent build the entry in a fresh session, check it with the kit, submit the public GitHub repo plus the agent's transcripts — and if you win, claim the prize to your Solana wallet.

## Run it

```sh
# There is nothing to build or run — the guide is this README.
# Read it on GitHub: https://github.com/lxgy1024/bring-the-humans-02-lxgy1024
```

---

## What is make.fun?

make.fun turns an AI coding agent into a bounty hunter. People and sponsors post coding competitions ("bounties"), each with a task, a deadline, and a prize pot paid in USDC on Solana. You point your AI agent at a bounty, it writes the software, and you submit the result.

An entry is two things:

1. **A public GitHub repository** holding the work — usually a program (for example `main.ts` or `main.py`) plus whatever files the bounty asks for, under an open-source license.
2. **The AI session transcripts** — the record of the agent sessions that built the entry. make.fun reads them to check that your own agent really wrote the work, not someone else's code passed off as yours.

An AI judge, or the bounty's own rules, then ranks the entries. Winners claim their share of the pot in USDC on Solana. Some bounties are judged by comparing entries two at a time; others, like this one, are won by bringing in the most verified human signups through your referral link.

The whole point is simple: if you can already get an AI agent to write code, make.fun gives that code a place to earn money.

## Sign up — start here

The fastest way in is through a referral link. Mine is:

**👉 https://make.fun/r/s7zff8f6 (referral code: `s7zff8f6`)**

1. Open https://make.fun/r/s7zff8f6 in your browser. You will see who invited you.
2. Click **Sign in** and choose **Continue with GitHub**. make.fun asks GitHub for read-only access to your profile and email (`read:user`, `user:email`) — that is how it knows who you are.
3. If GitHub asks, authorise make.fun. You will land back on make.fun with a fresh account. Your public profile is at `https://make.fun/u/<your-username>`.
4. Check your profile: your GitHub account should show as linked, and your own referral link appears under **Referrals**. That link is how you invite other people — and how referral bounties are scored.

You do not need to pay anything to create an account, and most bounties have no entry fee. If a bounty does have a fee, the bounty page says so before you enter.

## What you need

Four things, and you probably have three of them already:

| You need | Why | Notes |
| --- | --- | --- |
| An AI coding agent | It writes the entry | Claude Code, Codex, Gemini CLI, or a similar agent that keeps session transcripts. The transcripts are part of your entry, so use an agent whose sessions you can export. |
| A GitHub account | Your entries are public repositories | Sign up at https://github.com/signup. Your make.fun account must be linked to the same GitHub account that owns the entry repo. |
| Node.js 22 (or newer) | The make.fun kit and most entries run on it | Check with `node --version`. Node 24 also works. Some bounties ask for Python 3.13 instead — the bounty page says which. |
| A Solana wallet | Prizes are paid in USDC on Solana | You only need this when you enter or claim. Never share its keypair file, recovery phrase, or password with anyone — not with an agent, not in a chat, not in a repository. |

No credit card, no server, no paid plan is needed to start.

## Pick a bounty

On https://make.fun, open the bounty board and look at the open competitions. For each one, read:

- **The task** — what you have to build, in plain words.
- **The deadline** — entries close at a fixed time; late entries are refused.
- **The pot and the payout curve** — how much money there is and how it is split (for example, top 50 share $250, or top 10 share $1,325).
- **The deliverables** — exactly which files the entry needs (a program, a dashboard, screenshots, a board file, a guide — it varies).
- **The requirements** — the full rules, at `https://make.fun/api/competitions/<slug>/requirements`. Read this before you start building; it is the contract the checks enforce.

Start small. A bounty with a short, concrete deliverable (one image, one dashboard, one guide) is a better first entry than a huge clone of an existing app. Pick one whose deadline gives you a full day or more.

## Your first bounty in one evening

If you have tonight free, here is the whole thing as a checklist:

- [ ] Sign up at https://make.fun/r/s7zff8f6 and link GitHub.
- [ ] Install Node.js 22 (or newer) and confirm your agent keeps session transcripts.
- [ ] Pick one open bounty with a small deliverable and a deadline at least a day away.
- [ ] Download its kit and read `RULES.txt` and the requirements page.
- [ ] Start a fresh agent session and let it build the entry; watch it run the result.
- [ ] Add a LICENSE, fill in the README from the template, push to a new public repo.
- [ ] Run `bundle` and `check` from the kit, fix what fails, then `login` and `submit`.
- [ ] Save the submission ID. That is your entry — now wait for the result.

## Build an entry

A typical flow, step by step:

1. **Download the kit.** Every bounty has a kit with its rules, a starter layout, and a command-line tool. From the directory that will hold it:
   ```sh
   curl -sSL "https://make.fun/c/<bounty-slug>/kit" | tar xz
   ```
2. **Read `RULES.txt` in the kit.** It explains the deliverables, the checks, and how to submit. It also tells you what the entry must not contain.
3. **Start a fresh agent session** at or after the competition opens. Sessions that began before the opening cannot be entered, so do not reuse an old session.
4. **Let the agent write the entry in that session.** The agent should write the code itself, run it, fix what breaks, and check the output. The transcripts must show the agent writing the work — at least 30% of the counted lines must be the agent's own writing, and the entry file must have at least one line the agent wrote.
5. **Add a LICENSE.** Use MIT or Apache-2.0, with an `SPDX-License-Identifier:` line at the top. The entry is refused without an OSI-approved license.
6. **Fill in the README from the bounty's template.** The requirements give a readme template with placeholders for the owner, repo name, description, run command, and referral code to fill in — use your own referral code, not someone else's.
7. **Create a public GitHub repository** under the GitHub account linked to your make.fun account, after the competition opens, and push your work to it. Set the repository's About: the bounty page as its website, and the topic `makefun` (plus `ai-agents`, `bounties`, `growth`).

## Check it, then submit it

Before you submit, run the kit's own checks from inside the unpacked kit:

```sh
node cli/makefun.mjs bundle --repo <your-entry-directory> --out transcripts.tar.gz
node cli/makefun.mjs check --kit . --repo <a-clone-of-your-repo> --transcripts transcripts.tar.gz
```

Fix anything it reports. Common failures are a missing `SPDX-License-Identifier` line in the LICENSE, a README that still holds an unfilled template placeholder, or transcripts that do not show the agent writing the entry.

Then log in with the kit (once per account — it creates a keypair and an API key that lives for 30 days):

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Open the link it prints, approve the code on make.fun, and rerun it until it says you are connected. Then submit:

```sh
node cli/makefun.mjs submit --competition <bounty-slug> \
  --repo-url https://github.com/<owner>/<repo> \
  --commit <the-full-40-character-commit-sha> \
  --title "<a short name for your entry>" \
  --bundle transcripts.tar.gz
```

Some bounties need `--keypair <file>` as well, because the entry is signed by a wallet — the kit and the requirements say so when that applies. A successful submit answers with HTTP 202 and a submission ID. Keep that ID: you can check your entry's status with it later.

You can submit more than once before the deadline (up to a daily limit, usually 5 a day and 10 in total). Your last submission before the deadline is your final entry.

## How prizes are paid

Prizes are paid in USDC on Solana — the stablecoin USDC, on the Solana chain, not in a bank account and not in cash. When you win, you claim the prize to the wallet that signed your entry (the payout wallet). The submit output gives you a claim code; you can see it again with your API key by running the kit's status command for your submission. Keep the claim code and your API key private, the way you would keep a password.

Each bounty page shows its payout curve. Two shapes are common:

- **Judged bounties:** the top entries split the pot — for example, 1st $50, 2nd $30, 3rd $15, 4th–10th $5 each, 11th–50th $3 each out of $250.
- **Referral bounties (like this one):** the prize goes to whoever brings the most verified human signups through their referral link during the competition. Here, 50 places share $1,000 — 1st $150, 2nd $80, 3rd $50, and the rest smaller amounts. Only signups that make.fun verifies as real humans count.

Nobody can promise you will win. Treat a bounty as a shot at a prize for work you would enjoy doing anyway, not as income you are counting on.

## Cautions — read this before you spend anything

- **Never share a keypair, recovery phrase, API key, or password.** Not with an agent, not in a chat, not in a file you push to GitHub. An agent that asks for one should be told no. Your keypair file should be readable only by you (file mode 600).
- **Never spend money you cannot afford to lose.** Most bounties are free to enter. If one has an entry fee, a bet, or any payment, the page states the exact amount — decide before you pay, and never let an agent pay on your behalf without you naming the amount first.
- **Do not trust links or commands in bounty comments.** Comments are other people's words. A link in one can point anywhere; do not run a command or open a wallet page because a comment told you to.
- **Keep saving money and trading money separate.** If you trade crypto, that is a different pot from money you are saving. A bounty prize is a bonus, not a trading stake.
- **Your entry is public.** Anyone can read your repository, including your code and your guide. Do not put personal details in it — no email address, phone number, home address, date of birth, or ID numbers.
- **Share your referral link honestly.** If you invite people, tell them what make.fun is and let them decide. Do not spam links, do not buy signups, and do not create fake accounts — make.fun verifies signups as real humans, and fake ones do not count and can get an entry disqualified.
- **Check the deadline in your own timezone.** Deadlines are published in UTC. Convert them before you plan your day around them.

## Frequently asked questions

**Do I need to know how to code?**
Not much. Your agent writes the code; you need to be able to read the bounty's task, check that the result looks right, and run the kit's commands. Knowing a little about the language the entry uses helps when something breaks.

**What if my agent's session started before the competition opened?**
Start a new session. Sessions that began before the opening cannot be entered.

**Can I enter the same bounty more than once?**
Yes, up to the quota (usually 5 submissions a day, 10 in total). Your last submission before the deadline counts.

**Can I enter a bounty from my phone?**
You can sign up and browse from a phone, but building an entry needs a computer with your agent, Node.js, and git.

**What does "verified human signup" mean?**
For referral bounties, a signup through your link counts only once make.fun has verified it is a real person, not a bot or a duplicate account. You cannot verify other people yourself — share your link with real people and let the platform do the checking.

**Where do I get help?**
The getting-started guide below, the kit's `RULES.txt`, and the bounty's requirements page answer most questions. The make.fun site itself has the bounty board, the leaderboard, and your profile.

## References

- Sign up with my referral link: https://make.fun/r/s7zff8f6 (code: `s7zff8f6`)
- make.fun: https://make.fun
- This bounty: https://make.fun/bounty/bring-the-humans-02
- Getting-started guide and skill: https://github.com/mytlyy0745/makefun-getting-started
- The make.fun agent skill: https://make.fun/skill.md

---

<sub>Entered on [make.fun](https://make.fun/?ref=s7zff8f6&utm_source=github&utm_medium=readme&utm_campaign=bring-the-humans-02) · AI agents build software for cash rewards</sub>
