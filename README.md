# CapitalCompass

**Research with context. Decide with care.**

CapitalCompass is a Python investment research assistant with local or remote
AI models, market-data tools, opt-in web search and optional read-only portfolio
context through Plaid. Its chat-first workspace includes persistent history,
research settings, execution activity and a Stop control.

**This is the public landing-page repository, not the application source or a
hosted investment service. The application source remains private.**

## Request access

[Open the access-request form](https://github.com/limingchen-restart/capital-compass-public/issues/new?template=access-request.yml)
while signed in with the GitHub account you want invited.

1. Choose your intended use and optionally add brief, non-sensitive context.
2. The repository owner reviews the request manually. Approval is not guaranteed.
3. If approved, accept the GitHub invitation before opening the
   [private CapitalCompass repository](https://github.com/limingchen-restart/capital-compass).

**Requests and comments are public.** Your GitHub account identifies the requester;
no email address is needed. Do not post credentials, account numbers, holdings,
tax records or other private personal information.

GitHub usually returns **404** for a private repository if you do not have access.
This public request form does not change that behavior or automatically invite users.

## Scope and financial risk

The application currently supports research only. **No trades are executed.**
Trading and tax-document downloads/summaries are planned, not available, and
require additional permissions, safeguards and legal review.

AI output and market data may be inaccurate, incomplete or outdated. Research
suggestions are not orders, suitability determinations, professional financial/
legal/tax advice or guarantees. Investing involves risk of loss.

Local inference is not necessarily offline: research, broker and authentication
tools may contact external providers. Model licenses, provider credentials,
data-use rights and financial/regulatory obligations remain separate from
repository access. Approved users should review the application's financial-risk
and privacy notices before use.

## Publish the landing page

This repository contains only a static page and a public GitHub issue form.
There is no build step, JavaScript, external font, analytics script or signup
backend. Following the request link takes visitors to GitHub; its privacy
practices apply there.

Run these commands in PowerShell after reviewing the files:

```powershell
Set-Location "C:\Code\capital-compass-public"

git add -- README.md index.html .github\ISSUE_TEMPLATE
git diff --cached --stat
git commit -m "Add CapitalCompass landing page and access-request form" -m "Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com>"
git push -u origin main
```

Then, in **capital-compass-public**:

1. Ensure **Issues** is enabled under **Settings > General > Features**.
2. Open **Settings > Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose **main**, **/(root)** and **Save**.
5. Wait for GitHub's deployment, then check:
   https://limingchen-restart.github.io/capital-compass-public/
6. Test the access-request button while signed in and confirm the issue form opens.

The README also serves as a landing page on GitHub before Pages is enabled.
Publish only this repository's landing-page files; do not copy the private
application, chat databases, credentials or financial data into it.

### Local preview

From this repository's directory:

```powershell
python -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000/ and stop the server with Ctrl+C when finished.

## Maintainer: reviewing access requests

Review the issue author's GitHub account and stated purpose. To approve, open
the **private** repository's **Settings > Collaborators** (or its current access
management page), invite that account, and ask them to accept the GitHub
invitation. Close the request after resolution. Do not post private account
details or secrets in public comments.

Do not automatically grant access based on form submissions. A personal private
repository's collaborator access generally includes write permission; it is
not read-only merely because the application is read-only. If you need a Read
role for invited users, consider an organization-owned private repository and
its role-based access controls.
