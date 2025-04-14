# Velocity computations

## Capacity

### Definitions

- **Capacity**: the overall number of `man x days` during a sprint, in Working Days
- **Nominal capacity**: the capacity when every developer is fully available during the sprint

### Example

Given:

- A team of 4 developers (Bob, Alice, Ken & Barbie)
- 2 weeks sprints (`2 x 5 = 10` Working Days)

Then the **Nominal capacity** is `10 + 10 + 10 + 10 = 40` Working Days.

During the next sprint, Ken will be off one week. Then the **Capacity** is `10 + 10 + 5 + 10 = 35` Working Days.

### Exercice 1

Actually, Alice will be off two weeks as well. What is next sprint's **Capacity** ?

```

```

## Expected velocity

### Definitions

- **Nominal velocity**: the number of Story Points produced by the team at **Nominal capacity**
- **Expected velocity**: the number of Story Points the team expects to produce during the next sprint (forecast)
- **Actual velocity**: the number of Story Points actually produced by the team (measured)

### Computing the Expected velocity

```
Expected velocity = Nominal velocity / Nominal capacity x Capacity
```

🚨 Take the **Nominal velocity** as granted for now, we'll cover that later.

### Example

Given the following:

- **Nominal velocity**: 50 Story Points
- **Nominal capacity**: 40 Working Days
- **Capacity**: 30 Working Days

Then the **Expected velocity** is `50 / 40 x 30 = 37.5` Story Points.

### Exercice 2

Given the following:

- **Nominal velocity**: 50 Story Points
- **Nominal capacity**: 40 Working Days
- **Capacity**: 35 Working Days

What is the **Expected velocity**?

```

```

### Exercice 3 (wrap up)

Given the following:

- A team of 4 developers (Bob, Alice, Ken & Barbie)
- 3 weeks sprints
- **Nominal velocity**: 70 Story Points
- Bob & Alice are off next sprint

What is the **Expected velocity**? Please proceed step by step.

```

```

## Nominal velocity

### Computing Nominal velocity from Actual velocity

```
Nominal velocity = Actual velocity / Capacity x Nominal capacity
```

### Example

Given the following:

- **Nominal capacity**: 40 Working Days
- **Capacity**: 35 Working Days
- **Actual velocity**: 40 Story Points

Then the **Nominal velocity** is `40 / 35 x 40 = 45.7 ~ 45` Story Points (you should be conservative and floor the value).

### Exercice 4

Given the following:

- **Nominal capacity**: 40 Working Days
- **Capacity**: 20 Working Days
- **Actual velocity**: 30 Story Points

What is the **Nominal velocity**?

```

```

### Exercice 5 (wrap up)

Given the following:

- A team of 4 developers (Bob, Alice, Ken & Barbie)
- 3 weeks sprints
- Bob & Alice are off half of next sprint
- **Actual velocity**: 30 Story Points

What is the **Nominal velocity**?

```

```

## Actually, the Nominal velocity is a decision

One should **not** compute their team's **Nominal velocity** based on one single sprint (even a sprint at **Nominal capacity**), because this sprint might not be representative. The team might have under or over-performed due to external factors such as:

- There were very few meetings during this sprint (**Nominal velocity** will be overestimated)
- All the senior developers were on holliday during this sprint (**Nominal velocity** will be underestimated)

Consequently, you should compute a theoretical **Nominal velocity** and base your decision on that.

### Example

- Sprint #12: **Nominal velocity** = 40 Story Points
- Sprint #13: **Nominal velocity** = 38 Story Points
- Sprint #14: **Nominal velocity** = 37 Story Points
- Sprint #15: **Nominal velocity** = 44 Story Points
- Sprint #16: **Nominal velocity** = 38 Story Points

Sprint #15's velocity is surprisingly high in comparison to others. It should probably not be considered.

Then you should make a decision based on values: `40, 38, 37, 38`. It might be the mean value (`(40 + 38 + 37 + 38) / 4 = 38.25 ~ 38` Story Points), or the lowest value, `37` Story Points if you prefer a more conservative approach. That's up to you.

Finally, you should only consider the last few sprints (how many is up to you), because older sprints might not reflect the actual way the team works.

### Exercice 6

Given:

- A team of 4 developers (Bob, Alice, Ken & Barbie)
- 2 weeks sprints

And the following:

| Sprint #   | Capacity (Working Days) | Actual velocity (Story Points) |
| ---------- | ----------------------- | ------------------------------ |
| Sprint #1  | 40                      | 50                             |
| Sprint #2  | 35                      | 43                             |
| Sprint #3  | 30                      | 37                             |
| Sprint #4  | 30                      | 37                             |
| Sprint #5  | 40                      | 50                             |
| Sprint #6  | 38                      | 49                             |
| Sprint #7  | 40                      | 52                             |
| Sprint #8  | 40                      | 52                             |
| Sprint #9  | 40                      | 52                             |
| Sprint #10 | 40                      | 52                             |
| Sprint #11 | 25                      | 32                             |
| Sprint #12 | 30                      | 39                             |
| Sprint #13 | 40                      | 52                             |
| Sprint #14 | 35                      | 48                             |
| Sprint #15 | 40                      | 55                             |
| Sprint #16 | 35                      | 48                             |
| Sprint #17 | 40                      | 55                             |
| Sprint #18 | 40                      | 55                             |
| Sprint #19 | 25                      | 34                             |
| Sprint #20 | 20                      | 27                             |

Please make a decision for your team's **Nominal velocity**, and justify it.

```

```

## Suggested next steps

- Create a spreadsheet to ease those calculations for your team
- Compute/Decide your team's **Nominal velocity**
