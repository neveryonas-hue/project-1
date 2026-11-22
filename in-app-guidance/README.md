**Salesforce Lightning In-App Guidance & Suggest Related Articles on Cases**

> **About this sample:** Recreated in-app guidance based on content I built with the Salesforce Lightning In-App Guidance app to support the new process. The platform, company and data are fictional. AccountHub is modeled as a Salesforce page, and the secure payment tool is a separate web application, so the guidance covers the Salesforce side.

**See also:** [Knowledge article: Credit Card Payments and Changes with the SecurePay Link Tool](../README.md)

---

**The problem**

Agents on payment calls follow a security-sensitive process with several rules that are easy to miss: never take card numbers, the secure link expires in 15 minutes, and a card can't be replaced while auto-pay is on. Mistakes happen mid-call, when agents have no time to search an article.

**The approach**

Put short guidance on the page agents already use, at the moment they need it, and link to the full knowledge article for depth.

---

**1. Welcome prompt**

*Trigger: the agent opens the Payment Profile tab.*

<img width="600" alt="Welcome prompt on the Payment Profile page" src="inapp-1-prompt.png" />

A docked prompt reminds agents never to ask for card numbers. "Show me how" starts the walkthrough, and "Not now" lets experienced agents skip it. The Knowledge panel surfaces the full article.

**2. Walkthrough, step 1 of 2: auto-pay**

*Trigger: the agent selects "Show me how."*

<img width="600" alt="Walkthrough step 1 highlighting the Autopay row" src="inapp-2-autopay.png" />

The Autopay row is highlighted, and the message covers the four actions in one short sentence: check Autopay, set the date, add the email, save.

**3. Walkthrough, step 2 of 2: launch the tool**

<img width="600" alt="Walkthrough step 2 highlighting the launch button" src="inapp-3-launch.png" />

The launch button is highlighted, with the 15-minute expiry warning shown at the step where agents send the link.

**4. Targeted prompt: preventing a known error**

*Trigger: the agent is on a case where a saved card may be replaced.*

<img width="600" alt="Targeted prompt on the Autopay checkbox" src="inapp-4-preventive.png" />

This prompt attaches to the Autopay checkbox in AccountHub and stops the "can't remove card" error in the SecurePay Link tool before it happens. The "View full article" links to the full procedure.

---
---

**Suggested Articles on Cases**

**5. Suggested Articles in the Knowledge component**

*Trigger: the agent opens a Case.*

<img width="600" alt="Suggested Articles in the Knowledge component on a Case" src="inapp-5-related-articles.png" />

Customers wrote their own case subjects, so cases arrived in plain, first-person language like "I want to change the credit card on file." I configured Suggested Articles in the Salesforce Knowledge component on the Case record page. Based on the case subject and description, agents see the most relevant articles without leaving the case or searching. The best match appears first, and agents can attach an article to the case with one click.

---

**Reporting**

I built Salesforce reports in Lightning Experience to see how agents used the guidance and the articles:

- **Article views:** which articles agents opened most
- **In-app guidance clicks:** which prompts and buttons agents used
- **Search terms:** what agents typed into Knowledge search

Together, these showed where agents needed help and which content to improve. This sample doesn't show real figures.

---

**Design decisions**

- **Help where the work happens.** Guidance appears in AccountHub, where agents handle the payment, and articles appear on the Case, where the customer's request starts.
- **One action per message.** Each prompt covers a single step and stays short enough to read mid-call.
- **Warnings at the point of risk.** The link expiry and the auto-pay rule sit on the exact element where agents make the mistake.
- **Prevention over explanation.** The last prompt avoids an error instead of explaining it afterward.
- **Guidance and reference work together.** Prompts give a nudge in the moment, and Suggested Articles give the full procedure.
- **Titles in plain language.** Article titles use the words customers use, like "credit card" and "change," so the right article is easier to match to a case.
- **Link to depth.** Prompts stay brief and point to the knowledge article for the full procedure.
- **Easy to skip.** Agents can dismiss any prompt, so experienced staff aren't slowed down.

**How I measured it**



**Design decisions**

- **Triggered by the task.** Prompts appear where the work happens, not in a separate help area.
- **One action per message.** Each prompt covers a single step and stays short enough to read mid-call.
- **Warnings at the point of risk.** The link expiry and the auto-pay rule sit on the exact element where agents make the mistake.
- **Prevention over explanation.** The last prompt avoids an error instead of explaining it afterward.
- **Link to depth.** Prompts stay brief and point to the knowledge article for the full procedure.
- **Easy to skip.** Agents can dismiss any prompt, so experienced staff aren't slowed down.

**How I would measure it**

- Prompt views, "Show me how" starts, walkthrough completions and dismissals
- Clicks on "View full article"
- Call-handling errors that the guidance targets, such as expired links and failed card removals
- Salesforce Reporting after the first few weeks, used to shorten or retire prompts that aren't helping
