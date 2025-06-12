## Key Performance Indicators (KPIs) – Banking and Financial Services Project

Below are the KPIs calculated in this project using customer, loan, and deposit data. These KPIs help financial institutions monitor performance, customer behavior, and lending risk.

---

### Client & Account KPIs
| KPI | Description |
|-----|-------------|
| **Total Clients** | Total number of unique banking customers |
| **Estimated Average Income** | Average income across all clients |
| **Loyalty Classification Breakdown** | Distribution of clients by loyalty tier (e.g., Bronze, Silver, Gold) |
| **Clients by Occupation** | Grouping of clients based on their declared profession |
| **Clients by Nationality** | Segmentation of clients by country/national origin |

---

### Deposit & Account Balance KPIs
| KPI | Description | Formula / Example |
|-----|-------------|------------------|
| **Total Deposit Amount** | Combined value of all bank deposits | `SUM(bank_deposit)` |
| **Total Bank Deposit** | Amount held in term or time deposits only | `SUM(bank_deposit WHERE type = 'term')` |
| **Total Checking Account Amount** | Combined value in all checking/current accounts | `SUM(checking_account_amount)` |
| **Total Savings Account Amount** | Combined value in all savings accounts | `SUM(savings_account_amount)` |
| **Average Deposit per Client** | Measures financial activity | `Total Deposit / Total Clients` |

---

### 🏦 Lending KPIs
| KPI | Description |
|-----|-------------|
| **Total Loan Amount** | Total of all loans issued (personal, auto, home, etc.) |
| **Total Bank Loan** | Total of loans issued directly by the bank |
| **Total Business Lending** | Amount lent to businesses (SMEs or corporate) |
| **Bank Loan by Nationality** | Breakdown of loan value by customer nationality |
| **Bank Loan by Occupation** | Breakdown of loan amount based on client occupation |
| **Average Loan per Customer** | Helps assess average debt level per client |

---

### Credit Card KPIs
| KPI | Description |
|-----|-------------|
| **Total Credit Card Amount Issued** | Total value limit across all credit cards |
| **Total Credit Card Balance** | Total outstanding credit card balance |
| **Average Utilization Rate** | `(Credit Card Balance / Credit Card Limit) × 100` |

---

## Sample KPI SQL Queries

```sql
-- Total Clients
SELECT COUNT(DISTINCT client_id) AS total_clients FROM customer_data;

-- Total Deposit
SELECT SUM(bank_deposit) AS total_deposit FROM account_data;

-- Bank Loan by Nationality
SELECT nationality, SUM(bank_loan) AS total_loan
FROM loan_data
GROUP BY nationality;

-- Credit Card Balance
SELECT SUM(credit_card_balance) AS total_credit_card_balance FROM credit_data;
