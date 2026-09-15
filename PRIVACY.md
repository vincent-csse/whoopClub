# Whoop Club — Privacy Policy

**Last updated:** 15 September 2026

> **TODO before linking this in the WHOOP OAuth flow:** make this repository public, so
> that the link resolves for people outside the repo.

## What this is

Whoop Club is a personal, non-commercial tool. It connects your WHOOP account to an
AI assistant (Claude) running on your own computer, so you can ask questions about your
own training and recovery data.

It is not a WHOOP product and not endorsed by WHOOP. It is not a product of, or endorsed
by, any employer of the people who use it.

## What data it accesses

If you grant access, the app can read the following from your WHOOP account:

- Workouts and activity
- Physiological cycles (strain)
- Sleep
- Recovery
- Basic profile (name, email as held by WHOOP)

It requests **read-only** access. It cannot modify or delete anything in your WHOOP account.

## Where your data goes

This is the part worth reading carefully.

1. **WHOOP to your computer.** Data is requested directly by software running on your own
   machine, using your own authorisation. It does not pass through any server operated by
   the app owner.

2. **Your computer to Anthropic.** When you ask Claude a question about your data, the
   relevant data is sent to Anthropic's API as part of that conversation, because that is
   how Claude processes it. Anthropic's handling of it is governed by their own privacy
   policy and by the terms of whichever Claude plan you use. **If you are not comfortable
   with your health data being sent to Anthropic, do not use this app.**

3. **Nowhere else.** The app is not designed to transmit your data to any other party. It
   is built on the open-source `whoop-ai-mcp` package, maintained by a third party and
   installed from npm. Its behaviour is inspectable but is not audited or controlled by the
   app owner, and it could change in future versions.

## What is stored, and where

Everything is stored locally on your own computer:

- **Access and refresh tokens** at `~/.whoop-mcp/tokens.json`, with file permissions
  restricted to your user account (`0600`).
- **App credentials** in your Claude Desktop configuration file, in plain text.
- **Health data** is fetched on demand. Some summaries may be cached locally by the
  package during a session.

No database, server, or backup is operated by the app owner. There is nothing centrally
held to breach, and equally nothing centrally held to delete on request.

## What the app owner can and cannot see

**Cannot see:** your health data, your workouts, your recovery scores, or the content of
your conversations with Claude. None of it is routed through the owner.

**May be able to see:** aggregate information WHOOP shows to developers about the app
itself, such as how many accounts have authorised it and API call volumes. Treat the fact
that you authorised the app as visible to the owner.

## Revoking access

You can revoke access at any time from your WHOOP account's connected-apps settings. To
remove local traces afterwards, delete `~/.whoop-mcp/tokens.json` and remove the `whoop`
entry from your Claude Desktop configuration file.

## Children

Not intended for anyone under 16.

## Changes

This policy may change if the app changes. The date at the top reflects the current version.

## Contact

mostert.vincent12@gmail.com
