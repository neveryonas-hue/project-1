> **About this sample:** Recreated from knowledge content I wrote for a small and medium business (SMB) support team. The company (Feature Not a Bug Inc.), systems (AccountHub, SecurePay Link Tool) and processes are fictional. The structure, writing and design decisions reflect the real work.

- **Audience:** SMB support agents handling payment calls
- **Format:** Task-based knowledge article with expandable sections
- **Challenge:** To meet PCI compliance requirements, the company could no longer take card details over the phone. Agents needed to move customers to a secure-link process and expected pushback from customers less comfortable with technology.
- **Goal:** Help agents find the right procedure in seconds, and handle customer pushback with confidence
- **Outcome:** Agents had one clear reference and ready-made scripts for the new process, so they could guide customers through the secure link instead of taking card details by phone.


**See also:** [In-app guidance and Suggested Articles in Salesforce Lightning](in-app-guidance/README.md)

---


<img width="1520" height="200" alt="fake logo for fake company" src="https://github.com/user-attachments/assets/b8157fc8-145e-47c6-846e-ac07e6ae81f9" />

# Credit Card Payments and Changes with the SecurePay Link Tool

> Card details are no longer taken over the phone. This guide shows you how to send customers a secure link, take or update a card payment and answer the questions that come up.

---

## Can We Ask The Customer For Their Card Number?

**Never.** Feature Not a Bug Inc. uses the **SecurePay Link Tool** so customers enter their own card details through a secure form. After the customer enters their card, SecurePay sends AccountHub a token, a code that stands in for the card number, so agents never see or store the real card details. This meets *Payment Card Industry (PCI)* standards and protects customer information.

- These calls are handled by the SMB Support Team.
- Customers can also pay online and set up auto-pay through **My Account**. Mention it on every call.
- Tool not working? See *Troubleshooting* below.

> **Important:** The secure link is only active for **15 minutes**. Tell the customer when you send it.

---

## Prepare the Account in AccountHub

Log in to AccountHub in Salesforce Lightning, open the customer profile, and scroll to the **Payment Profile** section.

Expand the sections below for more information.

<details>
<summary><b>Optional. Set up auto-pay (if the customer wants it)</b></summary>

1. Check **Autopay** to use this card for automatic recurring payments.
2. Enter the preferred withdrawal date.
3. Enter the email address for the receipt.
4. Select the **Save** button.

<img width="600" alt="set up auto-pay" src="https://github.com/user-attachments/assets/766489ee-6a3e-4162-a3ac-1cdfec22c232" />

</details>

<details>
<summary><b>Launch the SecurePay Link Tool</b></summary>

**Choose how to launch the tool:**

- Select the **Make Credit Card Payment** button if a card is already on file.
- Select the **Set up Credit Card Profile** button to add, change or delete a card.

<img width="600" alt="launch securepay link tool" src="https://github.com/user-attachments/assets/17b8ce13-09bc-4028-8200-db7b2e650da1" />

</details>

---

## Choose What the Customer Needs

Expand the scenario below that matches the customer's request.

<details>
<summary><b>Customer wants to pay with their saved card</b></summary>

*Uses: Make Credit Card Payment*

If the profile has a saved card and the customer doesn't want changes:

1. Confirm the **last 4 digits** of the card.
2. Enter the payment amount (full or partial).
3. Select the **Pay Now** button.

A new window opens with a **confirmation number**. Give it to the customer.

> **Note:** You don't need to authorize the caller for this step.

<img width="600" alt="make a credit card payment" src="https://github.com/user-attachments/assets/d396b36e-b759-4214-8eb6-65c79cb79654" />

</details>

<details>
<summary><b>Customer has no card on file</b></summary>

*Uses: Set up Credit Card Profile*

If no profile exists, you'll see a setup screen after selecting **Set up Credit Card Profile**.

1. Authorize the customer.
2. Select the **Add Card** button.
3. Check the **Pre-Auth Flag**  box if the customer wants automatic payments. This registers the card for auto-pay.
   > **Reminder:** Autopay must also be selected in AccountHub.
4. Send the secure link by **email** or **SMS**.

> **Important:** The link expires after 15 minutes. Let the customer know.

<img width="600" alt="no credit card profile" src="https://github.com/user-attachments/assets/0008f042-d088-4c9c-a2c9-514ac401022e" />

</details>

<details>
<summary><b>Customer wants to pay once with a different card</b></summary>

*Uses: Set up Credit Card Profile. The saved card stays as the default.*

1. Enter the payment amount. Full or partial payments are accepted.
2. Select **New Credit Card**.
3. Leave the **Save Card** box unchecked so the existing card stays as default.
4. Click either the **Send Email** button or the **Send SMS** button to send the secure link. 

<img width="600" alt="set up new card" src="https://github.com/user-attachments/assets/c1dfa500-3064-4216-b227-e28b9a7eb849" />

</details>

<details>
<summary><b>Customer wants to replace their saved card</b></summary>

*Uses: Set up Credit Card Profile. The new card becomes the default.*

1. Authorize the customer.
2. Enter the payment amount (full or partial).
3. Select **Credit Card** as the payment method.
4. Select **Delete Credit Card**, then the **Remove Card** button.

<img width="600" alt="removeexisting card" src="https://github.com/user-attachments/assets/19aabb03-3c35-43d3-b5c5-3a8012be0968" />

5. Check the **Save Card** box.
6. Click either the **Send Email** button or the **Send SMS** button to send the secure link. 

<img width="600" alt="send secure link" src="https://github.com/user-attachments/assets/1bc2d2bb-531e-4407-a07a-fdabc4ab5d66" />

> **Watch for this:** You'll get an error when removing a card if the customer is on auto-pay. Go back to AccountHub, edit the account and uncheck **Autopay**, then try again.

> **Note:** On an auto-pay account, sending a link to change card details **replaces** the card on file.

</details>

---

## What is the Customer Experience?

Expand the section below to understand what the customer sees after you send the secure link. Walk them through it if they're unsure.

<details>
<summary><b>The Customer Experience</b></summary>

**Step 1: Customer receives the link.** 
The link arrives by email or SMS, depending on what you selected. The customer selects it and lands on a secure form.

   <img width="355" height="387" alt="customer receives link" src="https://github.com/user-attachments/assets/0b6f9a3a-0312-4ad1-bdf5-e90fa0e6fc12" />

**Step 2: Customer completes the secure form.**
   
- *New profile:* the customer enters the payment amount.
- *Existing profile:* the amount is filled in from what you entered.
- The customer enters card details and selects the **Pay Now** button.
   
 
> **Note:** If you selected **Save Card**, the customer will see a message that the card will be saved as default and will replace any existing card.
 
**Step 3: Confirmation**
   
 A confirmation screen shows a confirmation number and a button to print the receipt.


<img width="600" alt="the customer experience" src="https://github.com/user-attachments/assets/452eacf0-298b-4839-aa4c-75395341129d" />

</details>

---
## Handling Customer Pushback

New processes take customers time to adjust to. Use these positioning statements as a starting point and make them your own.

<details>
<summary><b>Positioning Statements</b></summary>

**"This is extra work. I don't have time."**
> I understand it feels like extra effort, but it protects your card details and your privacy, and it takes under a minute. If you sign up for auto-pay, you won't need to do it every month.

**"Wasn't my card data secure before?"**
> Yes, it has always been secure. This adds one more step to strengthen that protection.

**"I don't have internet access right now."**
> No problem. You can pay on <b>My Account</b> using mobile data. We also accept electronic fund transfers. Email us your account number and we'll send the banking details.

**"Can't I just give you my card number?"**
> I'd like to make this easy for you, but I'm not able to take card numbers. To protect your privacy, I'll ask you to enter them yourself.

**"I don't know how. Can't you do it?"**
> I'm happy to walk you through each step, but I can't enter your details for you. A family member could help, or you can pay at your bank or through <b>My Account</b> once the link has expired.

</details>

## Troubleshooting
If you are still stuck after checking out the tips below, escalate to the Business Support Team lead.
<details>
<summary><b> Check out these tips</b></summary>

| Problem | What to try |
|---|---|
| Customer didn't get the link | Confirm the email or phone number on the profile, check spam, then resend. Only the newest link works. |
| Link says it has expired | Links last 15 minutes. Generate and send a new one. |
| Error when deleting a card | The account is on auto-pay. Uncheck **Autopay** in AccountHub, then retry. |
| Token field is empty after setup | Refresh the AccountHub screen. |
| Customer's card was replaced unexpectedly | A link was sent with **Save Card** checked. Confirm with the customer and send a new link if needed. |

</details>

---
## How I Designed this Article
- **Task-based sections.** Agents arrive with a specific job, like "customer wants to pay with a different card." Each accordion matches one job so they can scroll, open and act.
- **Warnings where they matter.** The 15-minute expiry and the auto-pay error appear at the exact step where agents hit them, not in a separate list.
- **Show the customer's side.** Agents explain the process better when they know what the customer sees.
- **Scripts for hard moments.** Positioning statements reduce hesitation on calls where customers push back.




