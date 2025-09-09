- **`customer.subscription.created`** – triggered when a new subscription is created.
    
- **`customer.subscription.updated`** – triggered when a subscription is changed (plan upgrade/downgrade, quantity change, etc.).
    
- **`customer.subscription.deleted`** – triggered when a subscription is canceled.
    
- **`invoice.payment_succeeded`** – triggered when a subscription payment succeeds.
    
- **`invoice.payment_failed`** – triggered when a subscription payment fails.
    
- **`customer.subscription.trial_will_end`** – triggered 3 days before the trial ends (default, configurable).


It depends on **what you mean by “give user a product”** and the timing you want:

1. **`customer.subscription.created`**
    
    - Triggered **immediately when a subscription is created**, even if the payment fails.
        
    - ⚠️ Risk: The user may not have actually paid yet (e.g., if the first payment fails or is pending).
        
    - ✅ Use this if you want to **provision access immediately** and then handle failed payments separately.
        
2. **`invoice.paid`**
    
    - Triggered **after an invoice is successfully paid**.
        
    - This is a **safe point** to give the user a product because payment is confirmed.
        
    - ✅ Recommended if you want to **ensure the user only gets the product after successful payment**.
        
3. **`payment_intent.succeeded`**
    
    - Triggered when a **specific payment succeeds**, usually tied to one-time payments or the first payment of a subscription.
        
    - Can be useful if you’re **tracking payments independently** of invoices or subscriptions.
        
    - ⚠️ Slightly more low-level than `invoice.paid` for subscriptions; might require extra bookkeeping.
        

**💡 Best practice for subscriptions:**

- For subscriptions, **use `invoice.paid`** to provision the product.
    
- Optionally, listen to `customer.subscription.created` if you want to **pre-provision something** (like a trial access) before the first payment.