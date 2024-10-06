# Marketing Retention Analysis

This repository contains a Python script for simulating user retention data based on different marketing modes (SMS, OBD, Email). It also performs statistical analysis to evaluate the effect of marketing modes on user retention through A/B testing.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Data Generation](#data-generation)
- [Statistical Analysis](#statistical-analysis)

## Prerequisites

To run this script, ensure you have Python installed along with the following libraries:

- `numpy`
- `pandas`
- `scipy`

You can install the required libraries using pip:

```bash
pip install numpy pandas scipy
```

## Data Generation

- **Synthetic Data**: The script generates a dataset with 10,000 samples, including:
  - `user_id`: Unique identifier for each user
  - `date`: The date associated with the sample
  - `marketing_mode`: The marketing channel used (SMS, OBD, Email)
  - `retention_date`: The date when the user was retained, based on marketing mode retention probabilities
  - `retained`: A binary indicator (1 for retained, 0 for not retained)

Retention probabilities are defined as follows:
- SMS: 60%
- OBD: 50%
- Email: 40%

## Statistical Analysis

The script performs the following statistical analysis:

1. **Retention Rates Calculation**: The mean retention rates are calculated for each marketing mode.
  
2. **Chi-Square Test**: A Chi-Square test is conducted to determine if there is a significant effect of marketing mode on user retention.

   - If the p-value is less than 0.05, it suggests a significant effect.

## Example Output

The script displays the first few rows of the generated data and prints retention rates along with Chi-Square test results:

```
Generated Data:
    user_id        date marketing_mode retention_date  retained
0        1  01-01-2020            sms       02-01-2020         1
1        2  02-01-2020            obd       03-01-2020         1
2        3  03-01-2020          email               NaT         0
...
Retention Rates by Marketing Mode:
 marketing_mode
email    0.40
obd      0.50
sms      0.60

Chi-Square Test Results:
Chi2 Statistic: X.XXXX
p-value: Y.YYYY
Result: The marketing mode has a significant effect on retention.
```
