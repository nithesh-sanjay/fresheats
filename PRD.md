# FreshEats — Product Requirements Document (PRD)

> **What is this?** The master guide for our app. It summarizes the idea, who it's for, how it works, and links to the detailed guides for each part.

---

## The Idea

**FreshEats** is a mobile-friendly web app where software engineers in corporate IT parks can pre-order affordable, fresh, and nutritious meals from nearby vendors. Meals are prepared in advance and ready for pickup or desk delivery at a chosen time.

**Why?** No more long queues, no more unhealthy options during peak lunch hours, and no more missing meals because of busy schedules.

---

## Who It's For

**Primary users:** Software engineers and office workers at IT parks

**Who runs it:**
- **Food Vendors** — add meals and manage orders
- **Delivery Partners** — deliver meals to desks
- **Platform Admin** — manages everything

---

## The One Main Thing

A user can browse today's menu, pre-order a healthy meal, schedule it for pickup or delivery at a specific time, and pay — all in under a minute.

---

## Key Features

### For Office Workers
- Register and log in
- Browse healthy meals with nutrition info (calories, protein, fibre)
- Pre-order meals for pickup or desk delivery
- Choose a time slot
- Pay online or use a company lunch card
- Track order status in real time
- Earn healthy meal streaks and reward points
- Rate meals and suggest new dishes

### For Food Vendors
- Add and update meals
- Manage daily menus and stock
- Accept and prepare orders
- Update order status

### For Delivery Partners
- View assigned orders
- Accept deliveries (first come, first served)
- Update delivery status

### For Platform Admin
- Manage users and vendors
- View all orders and payments
- Manage reward points and offers
- View reports and analytics

---

## Does It Save Information?

**Yes.** We use **Supabase** — a free cloud database. We store users, meals, menus, orders, payments, streaks, reward points, meal suggestions, reviews, and delivery assignments.

👉 [See the full database plan → docs/database-plan.md](database-plan.md)

---

## Screens (Key Pages)

| Screen | What It Shows |
|---|---|
| Home / Menu | Today's meals with nutrition info, pastel Order buttons |
| Meal Details | Full description, ingredients, nutrition, reviews |
| Cart / Checkout | Order summary, time slot, address, payment |
| Order Tracking | Live status: Confirmed → Preparing → Ready/Delivered |
| My Orders | History of past and current orders |
| Streaks & Rewards | Your streak count, earned points, rewards |
| Profile | Name, email, preferences, payment methods |
| Suggest a Meal | Form to submit a new dish idea |
| Admin Panel | Manage meals, vendors, orders, payments |
| Vendor Dashboard | Menu management, order queue, inventory |
| Delivery Dashboard | Assigned orders, accept/update deliveries |

---

## Look & Feel

**Personality:** Fresh. Healthy. Quick.

**Mood:** Calm & Clean + Professional & Efficient

**Inspired by:** FreshToHome (fresh, healthy, trustworthy) + Notion (minimal, organized, distraction-free)

**First thing you see:** Today's menu — no login required to browse. Login only when you order.

**Signature element:** A subtle leaf motif 🌿 on every screen

👉 [See the full design guidelines → docs/design-guidelines.md](design-guidelines.md)

---

## Technical Choices

| Choice | What We're Using | Why |
|---|---|---|
| App type | Web app (works in any browser, including phones) | No app store needed, instant updates, works everywhere |
| Frontend | HTML + Tailwind CSS + DaisyUI | Free, easy, looks polished |
| Database | Supabase (PostgreSQL) | Free, no credit card, handles everything |
| Hosting | Vercel | Free, simple deployment, custom URL |
| Payments | Coming later (UPI/lunch card) | |

---

## How the App Works (Flow)

1. User opens the app → sees today's healthy menu with nutrition
2. Selects a meal → chooses pickup or desk delivery
3. Picks a convenient time slot
4. Confirms order → completes payment (or uses lunch card)
5. Kitchen receives the order → reserves/prepares the meal
6. Live updates: Order Confirmed → Preparing → Ready / Out for Delivery
7. User collects meal or receives at desk
8. Order marked completed
9. Streaks, reward points, and daily nutrition update automatically
10. User rates meal, gives feedback, suggests new dishes

---

## Tricky Moments (How We Handle Them)

| Situation | What Happens |
|---|---|
| Meal out of stock | Auto-stop orders, suggest similar meals |
| Two users want last meal | First to pay gets it; others see alternatives |
| Cancel after prep starts | No cancellation (or partial refund) |
| No delivery partner | Offer pickup or next available delivery slot |
| Missed pickup | Reminder sent → marked as missed if uncollected |
| Payment fails | Order not confirmed → retry or change method |
| Kitchen delay | Live updates with revised time |
| Two delivery partners | First to accept wins; order locked |
| Streak/points update | Only after order successfully completed |

---

## ⚠️ Important: Supabase Sleep Warning

Free Supabase projects go to sleep after **7 days** of inactivity. If saved data isn't loading (no menus, no orders, no login), log into [supabase.com](https://supabase.com) and **unpause your project** before any demo.

---

## Linked Guides

| Guide | What It Covers |
|---|---|
| [docs/database-plan.md](database-plan.md) | Everything stored, the rules, how to access |
| [docs/design-guidelines.md](design-guidelines.md) | Colours, fonts, button styles, layout |
| [docs/how-it-works.md](how-it-works.md) | *(Will be written after build is done)* |

---

*Last updated: July 28, 2026*
