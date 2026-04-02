# NEVER-AGAIN.md -- Kael's Failure Log (Real Examples)

## #1: The Config Crash (Day 1)
**What happened:** Used config.apply to update one setting. Config was invalid. Gateway crashed 225 times in a loop.
**Root cause:** No validation before applying.
**Rule:** NEVER use config.apply without verifying the diff first.

## #5: The PM2 Fork Bomb
**What happened:** PM2 set to restart on crash. No delay. No max attempts. Service crashed. PM2 restarted it. Exponential multiplication. System frozen.
**Root cause:** Default PM2 restart settings.
**Rule:** Always set max_restarts and restart_delay.

## #12: Plaintext Secrets
**What happened:** API keys in committed files. Stripe live keys. Bot tokens. In repos that could have been public.
**Root cause:** No secret scanning in commit pipeline.
**Rule:** Scan for secrets before every commit. Automate it.
