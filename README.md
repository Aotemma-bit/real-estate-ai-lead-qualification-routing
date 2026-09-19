# Real Estate AI Lead Qualification & Routing System

An AI-powered lead qualification and routing workflow for real estate businesses.

The system accepts incoming leads from different sources, normalizes and validates their information, uses Claude to extract qualification signals, applies a deterministic scoring engine, stores the lead in a CRM, and automatically routes the lead into the appropriate follow-up path.

## Overview

Real estate businesses can receive leads from many different sources:

- Website forms
- WhatsApp
- Facebook / Instagram
- Landing pages
- Manual submissions
- Other webhook-connected sources

The problem is that these leads can arrive in different formats and often require manual qualification before a sales team knows what to do with them.

This workflow creates a standardized pipeline:

**Lead Intake → Normalization → Validation → AI Qualification → Deterministic Scoring → CRM Storage → Lead Routing → Notification / Follow-up**

The goal is to reduce manual qualification work and make sure each lead enters the appropriate sales workflow.

---

## Core Workflow

### 1. Universal Lead Intake

The workflow begins with an inbound webhook.

The intake layer is designed to accept lead information regardless of the original source, provided the source can send data to the webhook.

The workflow then maps incoming information into a common lead structure.

Typical information can include:

- Name
- Contact information
- Lead source
- Property interest
- Budget
- Timeline
- Location
- Additional qualification information

---

### 2. Lead Normalization

Different lead sources may provide information using different field names and formats.

The normalization stage converts incoming information into a consistent internal lead structure.

This allows the rest of the workflow to operate on the same format regardless of where the lead originated.

**Example:**

```text
Facebook Lead
       ↓
Website Lead
       ↓
WhatsApp Lead
       ↓
Manual Lead
       ↓
Common Lead Schema
