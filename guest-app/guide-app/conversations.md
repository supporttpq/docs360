---
description: The Conversations section on the Guide App Home screen.
---

# Conversations

**Applies to:** Tourpaq Office · **Last reviewed:** 02-10-2026

{% hint style="danger" %}
**TO VERIFY** — The **Conversations** section of the Guide App has not been inspected for TQA-4298. The statements below are carried from the previous Guide App page, the Guest App page and the booking **Conversation** page.
{% endhint %}

#### Overview

**Conversations** is one of the ten sections on the Guide App **Home** screen. The Guide App supports guests directly through chat, and this section is the likely place where a guide reads and answers those chats.

In the Guest App, a guest starts a conversation with the guides of the booking destination from the **Chat** tab. The booking **Conversation** tab in Tourpaq Office shows the conversation log with the guest messages, agent replies, timestamps, read status and who handled the thread.

{% hint style="danger" %}
**TO VERIFY** — Is **Conversations** where guides read and answer the Guest App chats? What does the guide see on the screen, and can the guide start a conversation?
{% endhint %}

#### Purpose

* Answer guest questions directly from the destination.
* Keep the conversation history on the booking, for support and auditing.

#### Preconditions

* The guest uses the Guest App and has a booking — see Guest App.
* The guide is assigned to the resort of the booking.

{% hint style="danger" %}
**TO VERIFY** — Which user rights does a guide need for **Conversations**, and does a guide see only the resorts of their guide team?
{% endhint %}

#### How-to

{% hint style="danger" %}
**TO VERIFY** — Steps for opening, answering and closing a conversation in the Guide App.
{% endhint %}

The routing of a guest message, as described for the Guest App:

| Guest situation                         | Who receives the message                                                           |
| --------------------------------------- | ---------------------------------------------------------------------------------- |
| The booking is in the future            | All guides and admin users. The first guide who answers picks up the conversation. |
| The guest is already at the destination | All guides on that resort.                                                         |

#### Field Reference

{% hint style="danger" %}
**TO VERIFY** — Fields and options that control **Conversations**, and what the guide sees when there are no conversations.
{% endhint %}

#### Related pages

* Guide App
* Conversation (booking)
* Guest App
