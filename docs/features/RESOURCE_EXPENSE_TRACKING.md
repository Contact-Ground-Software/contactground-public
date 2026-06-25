# Resource Expense Tracking

Resource Expense Tracking lets organizations record entered aircraft/resource expenses, connect approved credit requests to expense records, and use resource-specific forecast pages for cost-per-hour planning.

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

Each category has a default cost type of `Fixed` or `Variable`. New and edited expenses default to the selected category's value, but the expense form can override the cost type for an individual expense. Manage organization categories from the Expenses page using `Manage Categories`.

## 4. Expense Entry

Use `Expenses` to enter standalone expenses without a credit memo.

Typical fields:

1. Resource
2. Category
3. Amount basis: `Total amount`, `Recurring`, or `Per flight hour`
4. Amount or hourly rate
5. Date
6. Frequency for recurring entries (`Weekly`, `Monthly`, or `Annual`)
7. Effective start/end dates for recurring and per-flight-hour entries
8. Vendor/reference when useful
9. Optional description

Use `Recurring` for real-world fixed costs such as hangar rent, loan payments, insurance, subscriptions, or annual inspections. The report prorates recurring entries across the overlap between the entry's effective dates and the selected report date range.

Use `Per flight hour` for saved expenses or reserves that should be materialized from submitted flight hours. Fuel and oil planning should generally come from actual receipts or selected forecast rows rather than hard-coded burn assumptions in the expense report.

Mobile users with access can also open `More` -> `Resource Expenses` to enter expenses and view compact summaries.

## 5. Credit Request Expenses

When Expense Management is enabled, approving a credit request also creates a linked expense entry.

During approval, select:

1. Expense resource
2. Expense category
3. Fixed or variable cost type
4. Expense date

The member credit and QuickBooks credit memo workflow remain separate from the internal resource expense report.

## 6. Maintenance Costs

Maintenance reminders and estimated maintenance costs are managed together from the resource maintenance page:

`Resource` -> select resource -> `Manage Maintenance & Costs`

Each maintenance item can include:

1. Reminder tracking by hours or date
2. Estimated expense amount
3. Expense category
4. Fixed or variable cost type
5. Notes
6. Whether the item is included in cost forecasts

Hour-based and date-based reminder modes remain mutually exclusive. If a maintenance task needs both, create two maintenance items.

Estimated maintenance costs do not appear as actual expenses in the Resource Expenses report. Variable estimates are planning inputs for resource cost forecasts. Fixed estimates are also included in the organization monthly dues forecast.

## 7. Resource Expenses Report

`Reports` -> `Resource Expenses` is an entered-expense report. It includes manual expenses, approved-credit-request expenses, and materialized recurring/per-flight-hour saved expense rows for the selected range.

The report includes:

1. Total entered expenses over time
2. Fixed vs. variable expense split
3. Expenses by category
4. Expense Pareto chart
5. Expense entry details and formulas

Filters include date range and resource. Predictive maintenance, automatic fuel/oil projections, available funds, and suggested hourly rates are intentionally not shown on this report.

## 8. Cost Per Hour Forecasting

Cost-per-hour planning is resource-specific:

`Resource` -> select resource -> `Forecast Cost Per Hour`

The resource page also shows a compact `Cost Per Hour` card with the current billing hourly rate and recent actual entered expense per submitted flight hour.

The forecast page is on-demand and does not save scenarios. It lets the user:

1. Include or exclude existing maintenance items with estimated costs.
2. Select existing entered expenses for planning.
3. Add temporary forecast-only rows.
4. Choose forecast flight hours.

Forecast output separates:

1. Fixed costs for resource-level context.
2. Variable/reserve costs divided across forecast flight hours.
3. Per-flight-hour expenses added directly to the hourly rate, regardless of whether their category is fixed or variable.

When Expense Management is enabled, organization administrators can open the monthly dues forecast beside the Monthly Member Rate setting. It includes fixed costs across all resources, prorates recurring expenses over the forecast period, adds forecast-enabled fixed maintenance estimates, and divides the result by forecast months and current members.

## 9. Best Practices

1. Track recurring fixed costs monthly so historical reports reflect real ownership cost.
2. Enter variable costs close to when they happen.
3. Keep maintenance item estimated costs current as quotes and due dates change.
4. Use resource forecasts before changing published hourly rates.
5. Use the organization monthly dues forecast before changing monthly member rates.
6. Keep Resource Expenses focused on entered expenses so actual reports remain auditable.

---

[Contact Ground Website](https://www.contactground.com)
