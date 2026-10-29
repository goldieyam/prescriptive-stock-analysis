# Stock Planning with Python

A simplified prescriptive-analysis coursework exercise that compares stock levels and identifies the quantity with the highest average profit under assumed demand scenarios.

> **Educational demonstration:** Results depend on the assumptions below and are not a real-world demand forecast.

## Purpose

Practise using Python loops, conditional logic and basic financial calculations to support a stock-purchasing decision.

## Assumptions

| Parameter | Value |
| --- | --- |
| Supplier cost | £3 per unit |
| Retail price | £5 per unit |
| Stock quantities tested | 30–50 units, inclusive |
| Demand scenarios | 30–50 units, inclusive |
| Scenario weighting | All 21 demand levels are equally weighted |
| Unsold stock | No recovery value within the model |

The exercise uses assumed values, not an external dataset. Demand is not predicted from historical sales.

## Method

For each stock quantity, the program:

1. Evaluates every demand level in the defined range.
2. Calculates units sold as the smaller of stock and demand.
3. Calculates profit as sales revenue minus the cost of all purchased stock.
4. Averages profit across the demand scenarios.
5. Retains the stock quantity with the highest average profit.

The calculation is:

`Profit = min(stock, demand) × retail price − stock × supplier cost`

This is an exhaustive search over a small set of discrete scenarios, rather than a trained machine-learning model.

## Results

With the supplied assumptions, the script produces:

```text
Optimal stock level: 38 units
Estimated average profit: £67.43
```

“Optimal” means the highest average profit among the tested stock quantities under equally weighted demand scenarios. It does not guarantee this profit in practice.

## Skills Practised

- Nested loops and range handling
- Conditional logic and minimum-value calculations
- Scenario analysis
- Profit calculation and averaging
- Selecting the best result within defined constraints

## Limitations

- Demand levels are assumed to be equally likely.
- Costs and selling prices remain fixed.
- The model excludes storage costs, spoilage, stockout penalties and other operational factors.
- Unsold stock has no recovery value in the calculation.
- Average profit does not describe the full range of possible outcomes.
- The denominator `21` is hard-coded and must be updated if the demand range changes.
- Exhaustive search is practical here but becomes less efficient as the problem grows.

## Running the Project

Run the script in Google Colab or another Python 3 environment.

No additional libraries or external data are required.
