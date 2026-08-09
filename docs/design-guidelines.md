# Design Guidelines — Plain English Guide

> **What is this?** This document explains the colours, fonts, and style choices for the app. Follow this to keep the look consistent everywhere.

---

## Brand Personality

**Three words:** Fresh. Healthy. Quick.

**Mood:** Calm & Clean + Professional & Efficient — trustworthy like a clean kitchen, fast like a productivity tool.

**Inspired by:** FreshToHome (fresh, healthy, trustworthy) + Notion (minimal, organized, distraction-free)

---

## Colour Palette

### Primary Colours
| Colour | Hex Code | Where It's Used |
|---|---|---|
| Fresh Green | `#4CAF50` | Main brand colour, healthy indicators, streaks |
| Clean White | `#FFFFFF` | Backgrounds, cards |
| Soft Black | `#1A1A2E` | Main text, headings |

### Accent Colours (Pastel CTA Buttons)
| Colour | Hex Code | Where It's Used |
|---|---|---|
| Mint Green | `#A8E6CF` | Primary "Order Now" button, success states |
| Soft Coral | `#FFB7B2` | Alerts, cancellations, missed orders |
| Warm Yellow | `#FFEAA7` | Reward points, streak badges |
| Light Lavender | `#DDA0DD` | Secondary actions, hints |
| Baby Blue | `#87CEEB` | Info labels, delivery status |

### Background Shades
| Colour | Hex Code | Where It's Used |
|---|---|---|
| Off White | `#F8F9FA` | Page background |
| Light Grey | `#E9ECEF` | Card borders, dividers |
| Soft Green Tint | `#E8F5E9` | Healthy meal highlights |

---

## Typography (Fonts)

### Headings: **Plus Jakarta Sans** (Bold)
- Modern, clean, slightly rounded — feels friendly but professional
- Used for: App name, section titles, meal names

### Body Text: **Inter** (Regular)
- Extremely readable, works great on phones
- Used for: Descriptions, labels, prices, nutrition info

### Where to Get Them (Free)
- Google Fonts: [fonts.google.com](https://fonts.google.com)
- Both are 100% free to use

---

## Buttons

### Primary Button (Order Now)
- **Background:** Mint Green `#A8E6CF`
- **Text:** Soft Black `#1A1A2E`, Bold
- **Shape:** Rounded corners (12px radius)
- **Size:** Large, full-width on mobile
- **Hover:** Slightly darker mint `#7DD3B0`
- **Pastel but unmissable** — soft colour, big size, clear text

### Secondary Button
- **Background:** Transparent with Light Grey border
- **Text:** Soft Black
- **Used for:** "View Details", "Cancel", less important actions

### Icon Buttons
- **Style:** Pastel circle backgrounds
- **Used for:** Cart, profile, notifications, back arrow

---

## Spacing & Layout

### Spacing System
- **Tight:** 8px — between small related items
- **Normal:** 16px — between sections
- **Loose:** 24px — between major sections
- **Extra Loose:** 32px — page margins

### Border Radius
- **Cards:** 16px — soft, approachable feel
- **Buttons:** 12px — slightly less rounded than cards
- **Images:** 12px — consistent with buttons
- **Badges/Pills:** 20px — fully rounded

### Shadows
- **Cards:** `0 2px 8px rgba(0,0,0,0.08)` — subtle lift
- **Buttons on hover:** `0 4px 12px rgba(0,0,0,0.12)` — slight elevation
- **Never use heavy shadows** — keep it clean

---

## Signature Element: The Fresh Leaf 🌿

Every screen has a small, subtle leaf motif:
- **On the logo:** A tiny leaf accent
- **On meal cards:** A small leaf icon for "healthy" meals
- **On streak badges:** Leaf grows as streak increases
- **On empty states:** A wilting leaf that perks up when you take action

This makes the app instantly recognizable and ties back to "fresh and healthy."

---

## Card Design (Meal Cards)

```
┌─────────────────────────────┐
│  [Meal Image]               │
│                             │
│  Meal Name                  │
│  Short description here     │
│                             │
│  🔥 350 cal  💪 25g protein │
│                             │
│  ₹149    [Pastel Order Btn] │
└─────────────────────────────┘
```

- **Image:** Top, full-width, 12px rounded corners
- **Name:** Bold, Plus Jakarta Sans
- **Description:** Grey, Inter Regular, 1-2 lines
- **Nutrition badges:** Small pills with icons
- **Price + Button:** Bottom row, price left, button right

---

## Status Colours (Order Tracking)

| Status | Colour | Meaning |
|---|---|---|
| Pending | Warm Yellow `#FFEAA7` | Waiting for confirmation |
| Confirmed | Mint Green `#A8E6CF` | Order accepted |
| Preparing | Baby Blue `#87CEEB` | Kitchen is making it |
| Ready | Fresh Green `#4CAF50` | Ready for pickup |
| Out for Delivery | Light Lavender `#DDA0DD` | On its way |
| Delivered | Fresh Green `#4CAF50` | Done! |
| Cancelled | Soft Coral `#FFB7B2` | Cancelled |
| Missed | Soft Coral `#FFB7B2` | Not collected |

---

## Mobile First

- **Design for phone first, then desktop**
- **Minimum tap target:** 44px (easy to tap with thumb)
- **Sticky bottom nav:** Home, Orders, Streaks, Profile
- **Bottom sheet for menus:** Like Blinkit/Uber — slides up from bottom

---

## Do's and Don'ts

### ✅ Do
- Use generous white space — let it breathe
- Keep text short and scannable
- Use pastel colours for backgrounds, bolder for CTAs
- Show nutrition info prominently (it's a health app!)
- Make the Order button always visible and obvious

### ❌ Don't
- Use dark backgrounds (keep it light and fresh)
- Crowd the screen with too many elements
- Use red for anything except errors/cancellations
- Use generic placeholder text
- Make users think — every screen should be obvious

---

## Quick Reference Card

| Element | Choice |
|---|---|
| Primary Font | Plus Jakarta Sans (Bold) |
| Body Font | Inter (Regular) |
| Primary Colour | Fresh Green `#4CAF50` |
| CTA Button | Mint Green `#A8E6CF` |
| Background | Off White `#F8F9FA` |
| Card Style | White, 16px radius, subtle shadow |
| Signature | Leaf motif 🌿 |
| Spacing | 8/16/24/32px system |
| Mobile Nav | Bottom sticky bar |

---

*Last updated: July 28, 2026*
