# How to Take Secure Card Payments

> **About this sample:** Recreated from knowledge content I wrote for a national telecom provider's business support team. The company (Feature Not a Bug Inc.), systems (AccountHub, SecurePay Link Tool) and processes are fictional. The structure, writing and design decisions reflect the real work.

- **Audience:** Business support agents handling payment calls
- **Format:** Task-based knowledge article with expandable sections
- **Goal:** Help agents find the right procedure in seconds, and handle customer pushback with confidence

---

## Can we ask the customer for their card number?

**Never.** Cedarline Business uses the **SecurePay Link Tool** so customers enter their own card details through a secure form. This meets Payment Card Industry (PCI) standards and protects customer information.

- These calls are handled by the Business Support Team.
- Customers can also pay online and set up auto-pay through **My AccountHub**. Mention it on every call.
- Tool not working? See *Troubleshooting* below.

> **Important:** The secure link is only active for **15 minutes**. Tell the customer when you send it.

Click a section below to expand it.

---

<details>
<summary><b>Task 1. Launch the tool from AccountHub</b></summary>

Log in to AccountHub, open the customer profile, and scroll to the **Payment Profile** section.

**Set up auto-pay (if the customer wants it):**

1. Check **Autopay** to use this card for automatic recurring payments.
2. Enter the preferred withdrawal date.
3. Enter the email address for the receipt.
4. Select **Save** (top right).

**Then choose how to launch the tool:**

- **Make Credit Card Payment** if a card is already on file.
- **Set up Credit Card Profile** to add, change or delete a card.

> **Good to know:** When Autopay is selected, the payment token is generated automatically by the tool and can't be edited. If you just created the profile, refresh the screen to see the token appear.




</details>

<details>
<summary><b>Task 2. Create a new payment profile</b></summary>

If no profile exists, you'll see a setup screen after selecting **Set up Credit Card Profile**.

1. Authorize the customer.
2. Select **Add Card**.
3. Check **Pre-Auth Flag** if the customer wants automatic payments. This registers the card for auto-pay. Autopay must also be selected in AccountHub.
4. Send the secure link by **email** or **SMS**.

> **Important:** The link expires after 15 minutes. Let the customer know.

<!-- Add screenshot: Create profile screen with Add Card and Pre-Auth Flag -->

</details>

<details>
<summary><b>Task 3. Update an existing profile</b></summary>

Use **Set up Credit Card Profile** in AccountHub when a profile already exists.

# One-time payment on a different card (keep the saved card as default)

1. Enter the payment amount. Full or partial payments are accepted.
2. Select **New Credit Card**.
3. Leave **Save Card** unchecked so the existing card stays as default.
4. Send the secure link by **email** or **SMS**.

# Replace the saved card with a new one

1. Authorize the customer.
2. Enter the payment amount (full or partial).
3. Select **Credit Card** as the payment method.
4. Select **Delete Credit Card**, then **Remove Card**.
5. Check **Save Card**.
6. Send the secure link by **email** or **SMS**.

> **Watch for this:** You'll get an error when removing a card if the customer is on auto-pay. Go back to AccountHub, edit the account and uncheck **Autopay**, then try again.

> **Note:** On an auto-pay account, sending a link to change card details **replaces** the card on file.

</details>

<details>
<summary><b>Task 4. Take a payment on a saved card</b></summary>

If the profile has a saved card and the customer doesn't want changes:

1. Confirm the **last 4 digits** of the card. If they want a different card, select **New Card** and follow section 3.
2. Enter the payment amount (full or partial).
3. Select **Pay Now**.

A new window opens with a **confirmation number**. Give it to the customer.

> **Note:** You don't need to authorize the caller for this step.

</details>

<details>
<summary><b>5. What the customer sees</b></summary>

After you send the secure link, here's the customer's experience. Walk them through it if they're unsure.

**Step 1: They receive the link.** It arrives by email or SMS, depending on what you selected. They select it and land on a secure form.

<img width="355" height="387" alt="06" src="https://github.com/user-attachments/assets/0b6f9a3a-0312-4ad1-bdf5-e90fa0e6fc12" />

**Step 2: They complete the form.**
- *New profile:* the customer enters the payment amount.
- *Existing profile:* the amount is filled in from what you entered.
- They enter card details and select **Pay Now**.

**Step 3: They get confirmation.** A confirmation screen shows a confirmation number and a printable receipt.

> **Note:** If you selected **Save Card**, the customer will see a message that the card will be saved as default and will replace any existing card.

<!-- Add screenshot: secure form and confirmation screen (fictional data) -->

</details>

<details>
<summary><b>6. Overdue, suspended and written-off accounts</b></summary>

There are four account statuses for accounts in arrears. Payment options depend on the status:

| Status | What the customer can do |
|---|---|
| **Overdue** | Pay through My Cedarline |
| **Suspended** | Full payment is required to restore services |
| **Payment arrangement (escalated)** | Call and speak with an agent to request an arrangement |
| **Written off** | Can't make payments. Can log in to My Cedarline, but all tabs are disabled with a message to call |

**For payment arrangements:**
1. Check the account history for any previously broken arrangements. Promises to pay are not accepted.
2. Email the Collections Team with the arrangement details to reactivate services.
3. Record the arrangement in AccountHub under **Activity Notes**.

</details>

<details>
<summary><b>7. Handling customer pushback</b></summary>

New processes take customers time to adjust to. Use these positioning statements as a starting point and make them your own.

**"This is extra work. I don't have time."**
> I understand it feels like extra effort, but it protects your card details and your privacy, and it takes under a minute. If you sign up for auto-pay, you won't need to do it every month.

**"Wasn't my card data secure before?"**
> Yes, it has always been secure. This adds one more step to strengthen that protection.

**"I don't have internet access right now."**
> No problem. You can pay on My Cedarline using mobile data. We also accept electronic fund transfers. Email us your account number and we'll send the banking details.

**"Can't I just give you my card number?"**
> I'd like to make this easy for you, but I'm not able to take card numbers. To protect your privacy, I'll ask you to enter them yourself.

**"I don't know how. Can't you do it?"**
> I'm happy to walk you through each step, but I can't enter your details for you. A family member could help, or you can pay at your bank or through My Cedarline once the link has expired.

</details>

<details>
<summary><b>8. Troubleshooting</b></summary>

| Problem | What to try |
|---|---|
| Customer didn't get the link | Confirm the email or phone number on the profile, check spam, then resend. Only the newest link works. |
| Link says it has expired | Links last 15 minutes. Generate and send a new one. |
| Error when deleting a card | The account is on auto-pay. Uncheck **Autopay** in AccountHub, then retry. |
| Token field is empty after setup | Refresh the AccountHub screen. |
| Customer's card was replaced unexpectedly | A link was sent with **Save Card** checked. Confirm with the customer and send a new link if needed. |

Still stuck? Escalate to the Business Support Team lead.

</details>

---

## How I designed this

- **Task-based sections.** Agents arrive with a specific job, like "customer wants a new card." Each accordion matches one job so they can scroll, open and act.
- **Warnings where they matter.** The 15-minute expiry and the auto-pay error appear at the exact step where agents hit them, not in a separate list.
- **Show the customer's side.** Agents explain the process better when they know what the customer sees.
- **Scripts for hard moments.** Positioning statements reduce hesitation on calls where customers push back.
- **Edge cases separated.** Overdue and written-off scenarios live in their own section so they don't clutter the main path.
