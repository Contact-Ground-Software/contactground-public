# Resource Expense Tracking

Resource Expense Tracking lets organizations track actual and predicted aircraft/resource expenses, then use those costs to support hourly-rate planning.

## 1. Enable the Feature

An owner or admin can turn the feature on from:

`Organization` -> `Expense Management`

When disabled, expense screens and expense reports are hidden and credit request approval works as it did before.

## 2. Who Can Use It

The feature is available to:

1. `Owner`
2. `Admin`
3. `Operations`
4. `Accounting`

## 3. Expense Categories

Contact Ground creates default aviation categories the first time the feature is used, including:

- Aircraft loan
- Hangar rent
- Insurance
- Fuel and oil
- Ramp and facility fees
- Maintenance
- Upgrades
- Other

Each category has a default cost type of `Fixed` or `Variable`.

## 4. Manual Expense Entry

Use `Reports` -> `Resource Expenses` to enter standalone expenses without a credit memo.

Typical fields:

1. Resource, or `Unassigned`
2. Category
3. Fixed or variable cost type
4. Amount basis: `Total amount`, `Recurring`, or `Per flight hour`
5. Amount or hourly rate
6. Date
7. Frequency for recurring entries (`Weekly`, `Monthly`, or `Annual`)
8. Effective start/end dates for recurring and per-flight-hour entries
9. Vendor/reference when useful
10. Description

Use `Recurring` for real-world fixed costs such as hangar rent, loan payments, insurance, subscriptions, or annual inspections. The report prorates recurring entries across the overlap between the entry's effective dates and the selected report date range. For example, `$225/month` over a full year contributes `$2,700`.

Use `Per flight hour` for planning reserves such as `$6/hr` for future avionics updates, `$10/hr` for maintenance reserve, or other costs that should scale with aircraft use but are not directly inferable from actual receipts. Per-flight-hour expenses require a resource because the report multiplies the rate by that resource's usage hours in the selected report period.

Do not enter fuel burn or oil consumption as manual per-flight-hour planning expenses. Enter actual fuel/oil receipts as `Total amount` expenses or approve member credit requests into the `Fuel and oil` category. When a report extends into the future, Contact Ground estimates future fuel/oil operating cost from recent actual fuel/oil dollars divided by recent submitted flight hours, then applies that cost per hour to projected future usage.

When the selected report range extends into the future, per-flight-hour expenses use recorded usage for elapsed dates and projected usage for future dates. If the selected date range already has actual usage, Contact Ground derives the projection from the elapsed portion of that same selected range. For example, a `Jan 1` through `Dec 31` report viewed in mid-June uses actual usage from `Jan 1` through mid-June to estimate usage for the rest of the year. This keeps annual planning aligned with the selected planning period instead of over-weighting a short recent burst of flying.

If the selected range is entirely in the future, or the elapsed part of the selected range has no actual usage, Contact Ground falls back to recent flight history. Fuel/oil projections use the same projected usage model, but the hourly cost is calculated from recent actual `Fuel and oil` expense history instead of user-entered fuel burn, fuel price, or oil consumption assumptions.

Mobile users with access can also open `More` -> `Resource Expenses` to enter expenses and view compact summaries.

## 5. Credit Request Expenses

When Expense Management is enabled, approving a credit request also creates a linked expense entry.

During approval, select:

1. Expense resource
2. Expense category
3. Fixed or variable cost type
4. Expense date

The member credit and QuickBooks credit memo workflow remain separate from the internal resource expense report.

## 6. Predicted Maintenance Costs

Predicted maintenance costs are tied to maintenance reminders/items. These are planning entries for future maintenance such as annual inspections, oil changes, engine overhaul reserves, or system upgrades.

Reports include predictive maintenance automatically when the selected date range extends into the future. Predictive maintenance is only counted for future dates.

Maintenance reminders predict or identify when work is due, but they do not provide a dollar amount by themselves. To include future maintenance dollars in expense reports or suggested hourly rates, add a predicted maintenance cost entry for the maintenance item.

For hour-based maintenance items, such as an engine overhaul due at a specific aircraft hour reading, the predicted cost entry can be saved without an expected date. Contact Ground will estimate the expected date from the maintenance item's due hours, the resource's current hours, and recent average usage. If the maintenance item is date-based, the item due date is used. If neither a due date nor a calculable hour-based prediction is available, enter an expected date manually.

## 7. Reports

`Reports` -> `Resource Expenses` includes:

1. Total expenses over time
2. Fixed vs. variable expense split
3. Expenses by resource
4. Expenses by category
5. Expense Pareto chart
6. Suggested hourly resource rates

Filters include date range, resource/all resources, category, and cost type.

The selected date range controls both which expenses are counted and how future usage is estimated:

1. Historical portions of the range use actual submitted flight hours.
2. Future portions of the range use projected hours.
3. If the range spans past and future dates, projected hours are based on the average usage from the elapsed portion of that selected range.
4. If the range is future-only, or has no actual usage yet, projected hours fall back to recent usage history.
5. Recurring expenses are prorated only for the part of the recurring entry that overlaps the selected range.
6. Predicted maintenance costs are included only when their expected date falls within the future portion of the selected range.

The bottom of the report includes a calculation summary that shows:

1. Usage hours by resource.
2. Each total, recurring, per-hour, usage-projection, and prediction row, the formula used, and the amount included in the report.

## 8. Available Funds in Hourly Rate Planning

The suggested hourly-rate report has an `Available Funds` input for reserves or cash already available for the selected planning period.

How it works:

1. For a single resource, available funds are subtracted from that resource's expenses before calculating the suggested hourly rate.
2. For all resources, available funds are allocated proportionally by each resource's share of expenses.
3. The report shows gross expenses, funds applied, net expenses, usage hours, and suggested hourly rate.
4. If a resource has expenses but no usage hours, the report shows a warning instead of a rate.

## 9. Best Practices

1. Track recurring fixed costs monthly so the rate model reflects real ownership cost.
2. Enter variable costs close to when they happen.
3. Record future maintenance estimates early, then refine them when quotes arrive.
4. Use available funds only for money intentionally available to offset the planning-period expenses.
5. Review suggested rates before changing published hourly rates.

---

[Contact Ground Website](https://www.contactground.com)
