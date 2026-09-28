# ChatDaddy

Run your ChatDaddy inbox from a conversation with Claude. Ask in plain English
and Claude does the work in your own team: sends and searches messages, finds and
tags contacts, fires bots, sets keyword replies and after-hours replies, runs
broadcasts, manages CRM tickets and webhooks, and checks why a channel stopped
sending.

It works across the channels your team has connected — WhatsApp, WhatsApp
Business API, Instagram, Messenger, SMS, email and web chat. Messaging is
deepest on WhatsApp; contacts, tags, tickets, bots and keyword replies apply to
every channel.

## Set it up

1. In ChatDaddy, open **Developer → API Tokens → Create** and copy the token. It
   starts with `apit_`, and it decides which team Claude works in.
2. Install this plugin and paste the token when Claude asks for it. The token is
   masked and stored in your system's credential store, never in a settings file.
3. Ask for something, for example *"list my ChatDaddy channels"*.

## Use it

Some things people ask for:

- "send 'your order shipped' to 6591234567"
- "find everyone who asked about delivery this week and tag them"
- "when someone sends 'price', reply with the pricing bot"
- "create a campaign for everyone tagged vip, 5 seconds apart, Friday 10am"
- "who did we message yesterday, and did it deliver?"

Claude asks you to approve anything that sends, changes or deletes before it
happens.

## What it runs, and what it sends

This plugin starts the published npm package
[`@chatdaddytech/mcp-server`](https://www.npmjs.com/package/@chatdaddytech/mcp-server),
pinned to version 1.0.0, on your own computer. That server talks to the ChatDaddy
API at `api.chatdaddy.tech` using your token, and to nothing else.

The package has **no runtime dependencies**: everything it needs is bundled into
the published files, so installing it resolves nothing at install time and pulls
in no third-party code. `npm install @chatdaddytech/mcp-server` adds exactly one
package.

The plugin itself stores no data. What Claude reads to answer a question — a
chat, a contact, a campaign result — is sent to Claude in that conversation, the
same as any other tool you give it. Your token stays on your machine and is sent
only to ChatDaddy.

## Privacy Policy

ChatDaddy's privacy policy: https://chatdaddy.tech/privacy-policy

## Support

Questions and bugs: support@chatdaddy.tech, or the setup guide at
https://chatdaddymcp.tech
