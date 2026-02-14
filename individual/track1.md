# Churn Data Expectations

## 1) Source tables:
1. **Customer Master (CRM)**
   - **One row = one customer** (customer profile, demographics, signup date, status)

2. **Account / Subscription**
   - **One row = one account or subscription** (plan, contract term, start/end dates, current status)

3. **Billing & Payments**
   - **One row = one invoice per account** (charges, discounts, payment method, payment status)

4. **Product Usage (Service / Network / App telemetry)**
   - **One row = one customer-account per day/week/month** (data usage, minutes, logins, feature usage)

5. **Customer Support / Service Tickets**
   - **One row = one support interaction or ticket** (issue type, resolution time, status)

## 2) Connecting the data:
- **customer_id**: primary identifier across CRM and customer-level attributes  
- **account_id / subscription_id**: connects billing, plan, and service records (a customer can have multiple accounts)  
- **event_date / billing_month**: aligns time-based facts (usage, bills, tickets) to the prediction window  

## 3) Risks/ mitigation actions:
1. **Risk: Data leakage (using info that only exists after churn happens)**
   - **Mitigation:** enforce a strict cutoff date (features only from data available *before* the prediction date), build features using rolling windows (e.g., last 30/60/90 days), and exclude post-churn fields (e.g., cancellation reason, final invoice adjustments).

2. **Risk: Duplicate or inconsistent IDs (multiple systems, merges, reassignments)**
   - **Mitigation:** customer/account mapping, deduplicate using business rules (latest record, active status priority), and validate joins with row-count checks.
