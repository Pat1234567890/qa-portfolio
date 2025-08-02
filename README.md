# Sample Bug Reports

## Bug 1: Restaurant Name Overlaps Price
**Summary:** Restaurant name overlaps the “12 $” price label on the Dish Details screen.  
**Steps to Reproduce:**  
1. Launch the app in Android emulator  
2. Select “Tomato soup with croutons”  
3. Observe overlapping text and price  
**Expected:** Name and price are separate  
**Actual:** They overlap  
**Severity:** Medium  
**Screenshot:**  
(https://patrickkirkland3.atlassian.net/browse/ULABR-1)
---

## Bug 2: Delivery Fee Omitted
**Summary:** Order confirmation total shows only food subtotal (“12 $”) and omits the delivery fee.  
**Steps to Reproduce:**  
1. Launch the app and place an order for $12  
2. View Order Confirmation screen  
**Expected:** Total = $12 + delivery fee  
**Actual:** Total shows only “12 $”  
**Severity:** High  
**Screenshot:**  
(https://patrickkirkland3.atlassian.net/browse/ULABR-2)

---

## Bug 3: Missing Cooking Time on Tracking Screen
**Summary:** Order Tracking screen shows only delivery time (“13 s”), missing the cooking time.  
**Steps to Reproduce:**  
1. Place an order  
2. On Tracking screen, observe time metrics  
**Expected:** Both Cooking Time and Delivery Time lines  
**Actual:** Only Delivery Time appears  
**Severity:** Medium  
**Screenshot:**  
https://patrickkirkland3.atlassian.net/browse/ULABR-3

---

## Bug 4: Route Missing on Delivered Screen
**Summary:** “Order Delivered” screen map omits the route line and marker style deviates from spec.  
**Steps to Reproduce:**  
1. Complete an order and wait for delivery confirmation  
2. Observe the map display  
**Expected:** Green route line + styled marker per Figma  
**Actual:** Only marker present; no route line, wrong marker style  
**Severity:** Medium  
**Screenshot:**  
https://patrickkirkland3.atlassian.net/browse/ULABR-4


---  

