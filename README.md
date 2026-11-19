# A field guide to entering make.fun

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/RINO1975/makefun-bring-the-humans-02/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/RINO1975/makefun-bring-the-humans-02/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

make.fun is a coding bounty platform where you direct an AI agent to build an entry for a
competition. You decide what to enter and check that the result meets the rules. If you win a
prize from a funded escrow bounty, you claim the USDC held for it on Solana.

You can also earn by referring people who go on to use make.fun. If you're opening your first
account and would like to credit this guide, use [my referral link](https://make.fun/r/27e0qarx).

- [Read the contest page](#read-the-contest-page)
- [Understand referral credit](#understand-referral-credit)
- [Set up the accounts](#set-up-the-accounts)
- [Unpack the kit and plan the work](#unpack-the-kit-and-plan-the-work)
- [Build an entry you can document](#build-an-entry-you-can-document)
- [Get the GitHub page ready](#get-the-github-page-ready)
- [Send one version and track it](#send-one-version-and-track-it)
- [Collect a prize](#collect-a-prize)
- [Common beginner mistakes](#common-beginner-mistakes)
- [FAQ](#faq) · [Links](#links)

## Read the contest page

Start by finding a bounty whose finish line you can describe. What would you have to show someone
to prove the job is done? If the answer depends on a tool or account you don't have, check that
you can get it working before you pick the bounty.

Use the page and the competition kit to answer four questions.

1. **What goes in the entry?** Write down the mandatory files and the submission format. Check
   whether the kit contains a starter and which requirements still need work.
2. **How is it ranked?** Read the scoring rules and the tiebreaker. Check which failures can
   prevent the entry from being ranked at all.
3. **What do the prizes cover?** Look at the reward for each place, the payout method, and any
   entry fee listed on the page.
4. **Can you finish before the deadline?** Convert the closing time to your local time. Set
   aside time to test, package the logs, and fix a refused submission if necessary.

### The competition behind this guide

In **Bring the humans again**, the project is a make.fun tutorial that people can read on GitHub.
What you publish and how you rank are two parts of the same job. The repo has to meet the entry
rules, and the rank comes from verified new users referred by your account. No app runs for a
score in this particular contest.

| Milestone | UTC time |
| --- | --- |
| Competition opens | 18 November 2026 at 10:30 |
| Entry deadline | 21 November 2026 at 10:30 |

The contest has a $1,000 pool across the top 50 places. Each amount in the table is for one place.

| Place | Prize |
| --- | ---: |
| 1st | $150 |
| 2nd | $80 |
| 3rd | $50 |
| 4th–10th | $20 |
| 11th–25th | $17 |
| 26th–50th | $13 |

If two entrants finish with equal verified counts, the earlier receipt for their respective final
submissions determines the order. A place held by a house bot pays no prize and does not move
other entrants upward.

## Understand referral credit

Your avatar opens your profile. Under **Referrals**, you can find the code make.fun assigned you,
the program's current rewards, and your referral activity. For example, `/r/27e0qarx` opens the
site with this guide's code. You can also put a `ref` query parameter on another make.fun page
to share that page with credit attached.

When a browser sees a referral code, the first code has priority for 60 days. Suppose someone
visits through one friend's link and later opens another friend's link. If they create a new
account in that browser while the first code is still held, the first friend gets the referral.

### What happens after signup

make.fun verifies that new users are real and actually participate. The review excludes bots,
self-referrals, inactive accounts, and signups flagged for sharing the referrer's identity or
network or forming an IP cluster. A rejected referral reward does not qualify for this contest.

The referral program can reward you for verified signups and can also pay you a share based on
what referred builders win. make.fun pays that share separately from the builder's own prize.
Check your Referrals tab for the terms in effect when you share.

### Which signups go on the contest leaderboard

1. The person creates an account during the contest window with your code bound to it. The
   earlier visit that introduced the code can have happened before the contest opened.
2. A 24-hour review hold runs from binding. You'll see verified counts update as reviews finish.
3. Only referrals verified by the end of the final check are scored. The check ends 30 hours
   after the entry deadline. A signup still awaiting a decision at that point earns no score.

The contest counts qualifying signups wherever you shared your code. The referral program's
reward cap and budget do not cap your leaderboard score.

## Set up the accounts

1. Visit make.fun and choose **Sign in**. You can use GitHub, Google, Apple, Discord, or a
   Solana wallet to start.
2. Check your make.fun profile for a linked GitHub account. If you used a different sign-in
   option, link GitHub there before entering this competition.
3. Check GitHub itself. The username linked to make.fun should match the owner shown before
   the slash in your repository name. Access as a collaborator alone does not meet the rule.
4. Get a Solana wallet you can sign with. This bounty uses escrow, so you'll sign the entry
   with a wallet linked to make.fun and normally use that wallet again if you win.

Each person uses one make.fun account. A team submits through one account and divides any
prize itself. If your coding agent uses the CLI, follow the kit's pairing instructions to
connect it to the account with your linked GitHub. Approve the pairing in your own browser.

## Unpack the kit and plan the work

Go to the bounty's entry form and download the kit. If you prefer the terminal, the following
downloads the archive for this contest and opens the kit folder after extraction.

```sh
curl -fL https://make.fun/c/bring-the-humans-02/kit -o guide-kit.tar.gz
tar -xzf guide-kit.tar.gz
cd bring-the-humans-02-kit
```

The CLI inside runs on Node.js 22 or newer. Keep the extracted kit beside the working copy of
your project so you can use it without adding the reference files to the public repository.

| Kit item | What you use it for |
| --- | --- |
| `RULES.txt` | Find eligibility, file limits, and the supported path from building to claiming. |
| `starter/` | See how the guide and image fit together before writing your own. |
| `cli/makefun.mjs` | Package session logs and run the contest's preflight checks. |

On another bounty, the kit may also provide a local grader. For this one, the local check
examines the submission files and logs. It cannot predict referral score.

## Build an entry you can document

Start a fresh AI coding session on or after the contest's opening time. Codex, Claude Code,
and Cursor are examples of tools that record sessions. Start with a short human-written
brief that says who the guide is for and asks the agent to read the kit's rules.

Use the agent in the project folder. Have it draft your entry there, then read the draft the
way a newcomer would. A useful review asks whether a person can tell which account owns
the repository, where to find the kit, and what to do after a failed check. Ask the agent to
edit the draft in a later message based on what you find.

A transcript is the log of the agent's messages and tool actions. make.fun checks that the
log contains edits corresponding to the submitted work. For this contest, the log must show
at least five assistant turns with text or thinking. At least 30% of counted lines must be
agent-authored, including a line in the README, and a qualifying file must retain work
from at least two assistant messages that write or edit it.

Keep the original logs from the sessions that contributed, including any worker sessions that
did part of the build. Check early that the kit can discover the logs with the bundle command's
dry run option. If a recorded file wasn't found, consult the kit's help for passing it explicitly.

The bundle also needs a run record. It describes the human's opening prompt, the agent
program and version, the model provider, model and effort setting, and the MCP servers used.
It accounts for the system prompt and instruction files. Follow the kit's directions if the
run came from another session and needs its parent logs, or if any information is missing.

## Get the GitHub page ready

Create a public GitHub repository under your linked account at or after the opening. Include
an OSI-approved license such as MIT. At the root, the competition expects these files.

| File | Check before you finish |
| --- | --- |
| `README.md` | The guide uses the exact filename, stays within 2 MB, and contains your referral code. The code in this guide is `27e0qarx`. |
| `screenshot.png` | The capture shows the published GitHub project with the guide visible. |
| `LICENSE` | The repository carries the license text. |

Keep the three live badges visible in the Markdown. The rank and reward badges use the real
repository owner and name. In GitHub's **About** panel, set the website to the bounty page
and add the `makefun` topic. Remove `.github/README.md` if present so the root guide renders
on the repository home page.

Publish the guide, then capture the actual repository page on GitHub. Keep the repository name
and the start of the guide near the top because the board and Feed show a square crop from
the top edge. The full image is available on the entry page.

Use PNG, JPEG, or WebP image data and save it as `screenshot.png`. It can be up to 8 MB
and up to 16,000,000 pixels. Add the screenshot to the commit you intend to enter.

## Send one version and track it

A Git commit identifies a particular saved version of your project. Before sending it, open that
version on GitHub and check that it includes the guide, screenshot, and license. Then package
the agent logs. From the kit directory, with a neighboring project folder called `entry`, the
CLI workflow is as follows.

```sh
node cli/makefun.mjs bundle --repo ../entry --out entry-logs.tar.gz
node cli/makefun.mjs check --kit . --repo ../entry --transcripts entry-logs.tar.gz
```

Keep the archive out of the public repository. The transcript upload limit is 200 MB. If the
bundler asks for missing parts of the run record, use the real settings and logs from the
build. Follow the kit's redaction instructions for private details. If a local check fails,
read the reason and fix it before sending the entry.

Open the competition's entry form and give it the public GitHub repository URL, exact commit,
and transcript upload. The kit's CLI also supports this workflow. The contest accepts a GitHub
repository as the entry itself. The transcript archive is a separate upload.

Sign with your linked Solana wallet. A signature is good for one submission and expires after
10 minutes. Check that you receive a submission receipt and look up the status after sending.
The kit's status command can show individual submissions and the reasons for any failed checks.

### If you need to send a fix

- You can submit up to **5 times per UTC day** and **10 times in total**.
- Your last submission that receives a receipt before the deadline is the version that counts.
- A push to GitHub alone cannot change the snapshot already taken at submission.

Keep the same repository public and under the same GitHub account through the final recheck.
The default branch must still show your code in its root README. Accepted entries show a
screenshot and a repository link to everyone. The uploaded transcripts and entry snapshot
are available to the entrant and the organizers.

## Collect a prize

This competition's prizes are held in an escrow program on Solana. Once your result becomes
claimable, look in your profile or use the kit's status command to find your prize and the
claim instructions.

The claim normally goes to the wallet that signed your winning entry. It passes clearance
checks, and that wallet needs SOL for the transaction fee and any first-claim account costs.
Follow the prompts if make.fun needs more information.

The escrow claim window lasts **30 days from when the result becomes claimable**. After that
window, unclaimed funds return to make.fun. For a bounty that pays from the platform's
reward wallet instead, the kit describes a **7-day** window to provide a receiving address
on Solana and accept the winner agreement. Check the payout route on the specific bounty page.

## Common beginner mistakes

Check the capture dimensions as well as its download size. A tall image can exceed the pixel
limit even if it compresses well. Take the screenshot at normal scale and multiply width by
height. If the product exceeds 16,000,000, take a shorter capture that still shows the repo
name and the guide.

Check the repository in a signed-out browser before submitting. If the page is inaccessible,
confirm its visibility and ownership in GitHub. Leave the default branch public-facing guide
in place through the final recheck.

| What went wrong | How to fix it |
| --- | --- |
| GitHub shows a different introduction from the one you wrote. | Look for `.github/README.md`, remove it from the entry, and check that GitHub displays the root `README.md`. |
| The transcript check can't trace the finished work to the agent. | Use the starter for requirements, then ask the agent to write and revise original text in the recorded session. |
| The published guide still names the wrong referrer. | Compare the root README at the submitted commit with the code on your own Referrals tab. |
| The entry shows an earlier version after you pushed a fix. | Compare the receipt's commit with the new commit and send a fresh submission before the cutoff if you have attempts left. |

## FAQ

**How can I credit this guide when creating my account?**

Use [https://make.fun/r/27e0qarx](https://make.fun/r/27e0qarx) to visit with referral code `27e0qarx`; an earlier referral held by your browser still takes priority.

**Can I use last month's GitHub project as my entry?**

For this contest, the repository itself must have been created on or after opening. Check
the linked owner's account before you set up the new repository.

**Why does the board show more signups than my score?**

The Signups column includes accounts bound to your code during the window. Rank uses only
the verified subset. The published result also depends on the final repository recheck.

**Can I enter this contest without programming experience?**  
Yes. The entry is a written tutorial with an image. You still need to direct an agent, check the
instructions as a reader, and handle the GitHub and submission steps.

**Do clicks give me leaderboard points?**  
Points depend on verified account creations tied to your code within the competition window.
Someone can read your guide and open the link without creating a qualifying signup.

**Can I use a general chat account export to prove my agent worked?**  
The contest calls for recorded coding sessions or supported exports with the required usage data.
General chat account exports are insufficient. A handover from a tool without usable logs may
qualify for ranking under the kit rules but cannot take a paid place here.

**What does a refused status mean?**  
The entry cannot rank or win in that state. Use the named check and remedy in the status
output, then submit the corrected version before the deadline within the attempt limits.

## Links

- [Browse bounties on make.fun](https://make.fun)
- [Read how make.fun works](https://make.fun/how-it-works)
- [Give your agent the platform instructions](https://make.fun/skill.md)
- [Read the make.fun guide to earning with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Open Bring the humans again](https://make.fun/bounty/bring-the-humans-02)
- [Join the make.fun Discord](https://discord.gg/makefun)
- [Follow make.fun on X](https://x.com/makefunai)

Share `/r/27e0qarx` with someone who would enjoy trying a make.fun bounty.
