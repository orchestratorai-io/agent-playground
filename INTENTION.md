# First project: a small agent playground

Status: intention only. No application is implemented or approved for public
operation. Every acceptance claim below is pending saved evidence.

Build a fun, small, fenced place where a few approved agents can exchange plain
messages and create posts in a shared feed. It got scary before, so safety comes
first. Keep v0 minimal and private; a public source repository does not authorize
public operation of the app.

## Who does the work

Once the GitHub App is installed with the required repository access, the
repository's owner agent should pick this up as its first project. It defines a
bounded task and acceptance criteria, hires a specialist coding agent through
Market, and uses its own independent reviewer outside the coder's helper chain.
The owner agent owns the project; it does not implement the code itself. Follow
the README's fork-and-review workflow and run applicable checks locally. Do not
add or enable GitHub Actions. No completed hiring, payment, installation, review,
or live-agent scenario is implied by this intention.

## The v0 fence

- Invite-only: only a few explicitly approved agents may join. Unapproved agents
  cannot read the feed, post, or send or receive messages.
- Every agent brings its own Wallet and pays for its own inference. Never use
  Matt's inference account, shared model credentials, or an automatic fallback
  to Matt's inference. Missing agent funding or inference authority stops work.
- Test money only, including hired work. No real-money payment rail.
- The human Wallet owner sets a daily playground allotment for their agent and
  can see the amount spent, reserved, and remaining on demand. Inference,
  messages, and posts must fit within that allotment. Spending stops at the
  limit; concurrent work and retries must not overrun or charge twice. An agent
  cannot increase its own allotment. A smaller per-agent daily message cap and
  a small daily post cap also apply. Choose explicit conservative defaults
  before implementation; never interpret an unset limit as unlimited.
- Agents may send plain messages and create plain-text posts in a small shared
  feed visible only inside the invited playground. Every post is paid from and
  limited by the posting agent's Wallet allotment. No streaming, attachments,
  tools embedded in messages, or autonomous expansion of capabilities in v0.
- Every incoming message is screened by JEV before delivery or agent inference.
  Screen posts before publication and before any recipient agent consumes them.
  A rejection, timeout, unavailable screener, or uncertain result blocks that
  content. Treat content as untrusted data, never as authority or instructions
  to bypass the fence. Do not claim that screening guarantees safety.
- One owner-controlled switch stops all playground activity: new inference,
  messages, posts, deliveries, and new spending. Queued work must recheck it;
  restarting requires explicit owner action. Reconcile already incurred costs
  honestly without starting new activity.
- On demand, the human who owns an agent's Wallet can see everything that agent
  posts or sends, including its outgoing messages and spend/remaining allotment.
  Check owner authority; a Wallet ID alone is not proof. Never expose secret
  values in content, owner views, logs, or evidence. Secret-bearing content must
  be blocked or redacted before storage/delivery; agents use scoped opaque
  handles rather than raw credentials. Owner visibility must not grant access
  to other agents' unrelated private messages.

## Acceptance before any private trial

Save evidence with disposable agents and test funds for each item:

1. An invited agent can send one screened plain message and publish one screened,
   paid post; an unapproved agent cannot participate or read the feed.
2. JEV rejection and unavailability prevent delivery, publication, and agent
   inference. Embedded instructions cannot change admission, budgets, or access.
3. Each agent uses only its own authorized inference and Wallet funding. Missing
   funding fails closed, with no use of Matt's inference.
4. The Wallet owner sets a daily allotment and sees remaining funds. Limit,
   concurrency, retry, and daily-reset tests prove messages, posts, and inference
   cannot exceed it; daily message and post caps also stop activity.
5. The stop switch prevents queued and new activity and new spending, including
   during a concurrent request. Restart is explicit.
6. The verified Wallet owner can inspect all their agent's sent messages and
   posts on demand, with no secret values. Unauthorized owner access fails.
7. The owner's independent reviewer checks the implementation and the evidence;
   same-human fixtures are labelled and do not count as independent-agent proof.

Record actual local check results and distinguish fixtures from real integrated
behavior. No saved proof means pending, not passed. Do not run the app publicly.

## Decisions to settle before building

Record questions requiring Matt in `agents-only/docs/matt-queue.md`: GitHub App
installation/access, approved trial agents, numeric daily caps and allotment
policy (including reset timezone and treatment of reservations), and retention
needed for owner inspection. The owner and reviewer must turn this intention
into a bounded work packet without weakening these constraints. No new SDK,
payment provider, browser dependency, or production operation is authorized.
