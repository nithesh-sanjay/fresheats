# Database Plan — Plain English Guide

> **What is this?** This document explains what information our app stores and the rules it follows. Think of it as a blueprint for the app's memory.

---

## Where We Store Data: Supabase

**What is Supabase?** A free online database (like a super-powered spreadsheet in the cloud) that our app reads and writes to. No credit card needed.

**⚠️ Important:** Free Supabase projects sleep after 7 days of inactivity. Before any demo, log into [supabase.com](https://supabase.com) and unpause your project, or saved data features won't work.

---

## What We Store (Our Tables)

### 1. Users
| Field | What It Means |
|---|---|
| id | Unique ID for each person |
| name | Full name |
| email | Email address (used for login) |
| phone | Phone number |
| role | `worker`, `vendor`, `delivery`, or `admin` |
| reward_points | Total reward points earned |
| current_streak | Consecutive days ordering healthy meals |
| created_at | When they signed up |

### 2. Meals
| Field | What It Means |
|---|---|
| id | Unique ID for each meal |
| name | Meal name (e.g., "Grilled Chicken Bowl") |
| description | What's in it |
| price | Cost in local currency |
| calories | How many calories |
| protein | Protein in grams |
| fibre | Fibre in grams |
| ingredients | Full ingredient list |
| image_url | Photo of the meal |
| vendor_id | Which vendor created it |
| available_quantity | How many are left today |
| is_active | Whether it's currently on the menu |
| created_at | When it was added |

### 3. Menus
| Field | What It Means |
|---|---|
| id | Unique ID |
| meal_id | Which meal is on the menu |
| date | Which day this meal is available |
| special_price | Any discount for that day (optional) |

### 4. Orders
| Field | What It Means |
|---|---|
| id | Unique ID for each order |
| user_id | Who placed the order |
| meal_id | What meal they ordered |
| order_type | `pickup` or `delivery` |
| scheduled_time | When they want it |
| status | `pending` → `confirmed` → `preparing` → `ready` → `out_for_delivery` → `delivered` / `picked_up` / `completed` / `cancelled` / `missed` |
| delivery_location | IT park / floor / desk (if delivery) |
| total_amount | Final price paid |
| created_at | When the order was placed |

### 5. Payments
| Field | What It Means |
|---|---|
| id | Unique ID |
| order_id | Which order this payment is for |
| amount | How much was paid |
| method | `lunch_card`, `upi`, `card`, `cash` |
| status | `pending`, `completed`, `failed`, `refunded` |
| transaction_id | Reference number from payment provider |
| created_at | When payment was made |

### 6. Delivery Assignments
| Field | What It Means |
|---|---|
| id | Unique ID |
| order_id | Which order to deliver |
| delivery_partner_id | Who is delivering |
| status | `assigned` → `picked_up` → `delivered` |
| accepted_at | When the partner accepted |
| delivered_at | When it was delivered |

### 7. Meal Suggestions
| Field | What It Means |
|---|---|
| id | Unique ID |
| user_id | Who suggested it |
| meal_name | What they suggested |
| description | Their description |
| status | `pending`, `approved`, `rejected` |
| created_at | When suggested |

### 8. Reviews
| Field | What It Means |
|---|---|
| id | Unique ID |
| user_id | Who reviewed |
| meal_id | Which meal |
| order_id | Which order |
| rating | 1 to 5 stars |
| comment | Their feedback |
| created_at | When reviewed |

### 9. Reward Transactions
| Field | What It Means |
|---|---|
| id | Unique ID |
| user_id | Who earned/spent points |
| points | Positive = earned, Negative = spent |
| reason | Why (e.g., "order completed", "streak bonus") |
| created_at | When it happened |

---

## Main Rules

1. **Stock control:** When `available_quantity` hits 0, the meal stops showing as available. First to complete payment gets the last one.
2. **Order status flow:** Orders always move forward: `pending` → `confirmed` → `preparing` → `ready` → `out_for_delivery` → `delivered` → `completed`.
3. **Cancellation:** Allowed only while status is `pending` or `confirmed`. Once `preparing`, no cancellation or partial refund.
4. **Streaks:** Updated only after order status becomes `completed`.
5. **Delivery lock:** Once a delivery partner accepts, the order is locked to them — no one else can claim it.
6. **Missed pickups:** If not picked up within the time window, status becomes `missed` and streak is not updated.
7. **Payment first:** Order stays `pending` until payment status is `completed`.
8. **Users see only their own:** Workers see only their orders, points, and streaks. Vendors see only their meals and orders. Admin sees everything.

---

## How to Access

- **Supabase Dashboard:** Go to [supabase.com](https://supabase.com), sign in, and select your project
- **Table Editor:** Click "Table Editor" in the sidebar to view and edit data like a spreadsheet
- **Remember:** Unpause your project before any demo!

---

*Last updated: July 28, 2026*
