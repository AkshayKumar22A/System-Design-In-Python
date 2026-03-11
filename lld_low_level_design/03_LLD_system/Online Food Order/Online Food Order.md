# Practical Example: Online Food Order

Let's apply **classes and objects** to a real-world problem: building an order management system for a food delivery platform.

## The Scenario

A food delivery app needs to manage orders.

### Order Structure
- Each order belongs to a customer
- Contains a list of food items with prices
- Tracks whether it has been placed

Customers build their order by adding items one at a time, and once they're satisfied they place the order. After that, no more items can be added.

### Problem Without Classes
Without classes, you'd have separate arrays for order IDs, customer names, item lists, and totals with no clean way to enforce rules like _"don't add items after placing."

### Benefits of Using Classes
With classes, the `Order` owns its data and enforces invariants:
- `addItem()` works only **before** `place()`
- Invalid states are prevented by design

This makes the system cleaner, safer, and easier to maintain.