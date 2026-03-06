---
name: use-logrocket
description: Query LogRocket for session replays, metrics, issues, and user behavior using natural language. Use when debugging issues, analyzing feature usage, investigating errors, triaging problems, or understanding how users interact with your app.
---

# Use LogRocket

## When to use

- Debugging a user-reported issue or error
- Understanding how a feature is currently being used before making changes
- Triaging new issues and figuring out root causes
- Checking for regressions after recent deploys or commits
- Prioritizing what to work on next based on real user impact
- Investigating JavaScript errors, rage clicks, or dead clicks
- Analyzing post-launch behavior for a new feature
- Researching a specific user or account's sessions

## Instructions

1. Call the `use_logrocket` MCP tool with a natural language `query` describing what you want to know.
2. To continue the same conversation (e.g. follow-up questions, drilling deeper), pass the `chatID` from the previous response.
3. Be specific about what you want analyzed — mention URLs, click targets, user emails, time ranges, or custom events when possible.
4. Ask LogRocket to watch sessions when you need detailed, qualitative insights about user behavior.
5. Present results clearly to the user, including any session URLs, metrics, charts, or actionable insights.

## Example Prompts

- **Debug user-reported issues:** "User X reported a problem with checkout. Can you use LogRocket to watch their sessions and figure out the root cause?"
- **Understand feature usage:** "I'm about to work on the search feature — can you use LogRocket to help me understand how it's currently being used?"
- **Triage new issues:** "Can you look at LogRocket for new issues from the past week, try to figure out their root causes, and then suggest which ones I can fix?"
- **Check for regressions:** "Look at all commits from last week, and check LogRocket data to ensure they didn't introduce any regressions."
- **Prioritize your work:** "Use LogRocket to watch sessions and look at issues to figure out what is highest priority that I work on next."

## Suggested Automations

Because the MCP server can be called programmatically by AI agents, you can set up powerful automations that continuously leverage LogRocket data:

- **Research churning customers and low NPS scores:** Automatically pull LogRocket sessions for users who are churning or leaving low NPS scores to understand what went wrong in their experience.
- **Research new support tickets:** Connect to your help desk to automatically research incoming support tickets using LogRocket session data. LogRocket offers out-of-the-box integrations with Zendesk and Intercom to attach session replays directly to tickets.
- **Summarize user behavior for sales and customer success:** Automatically generate summaries of how key accounts are using your product, giving your sales and customer success teams actionable insights.
- **Connect LogRocket with your backend data:** Build a skill that allows your agent to correlate LogRocket frontend data with backend observability tools (e.g. Datadog MCP) for end-to-end debugging.
- **Run daily or weekly reports:** Schedule an agent to look for new issues and UX frustration signals on a recurring basis, so your team is always aware of emerging problems.
