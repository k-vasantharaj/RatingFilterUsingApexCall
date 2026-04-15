🚀 Account Rating Filter (LWC)

This project demonstrates filtering Account records by Rating using two different approaches in Lightning Web Components (LWC):

Imperative Apex Call
@wire (Reactive Apex)

It highlights the difference between controlled execution vs reactive data fetching.

📌 Features
Filter Accounts by Rating (Hot, Warm, Cold)
Dynamic UI rendering using SLDS
Badge styling based on rating
Loading spinner for better UX
Empty state handling
Error handling


🧠 Concepts Covered
Lightning Web Components (LWC)
Apex Integration
Imperative vs @wire
Conditional Rendering
Event Handling
Data Transformation (UI mapping)
SLDS Styling
🛠️ Components
1️⃣ accountRatingFilter (Imperative)

Approach: Imperative Apex Call

Data is fetched only when user clicks button
Full control over execution

Better for:
User-triggered actions
Conditional API calls

Key Logic:
getAccounts({ rating: this.rating })


Highlights:
Uses isLoading for spinner control
Handles success, error, and empty states explicitly
Transforms data to include badgeClass
2️⃣ accountRatingFilterWire (Reactive)

Approach: @wire

Data is fetched automatically when rating changes
Reactive and declarative
Less control compared to imperative
Key Logic:
@wire(getAccounts, { rating: '$rating' })
Highlights:
No button required
Automatic refresh on input change
Simpler but less flexible


⚖️ Imperative vs @wire
Feature	Imperative	@wire
Execution Control	✅ Full control	❌ Automatic
Trigger	Button click	Variable change
Use Case	User actions	Reactive UI
Error Handling	Manual	Built-in pattern

🎯 Key Learnings
Imperative calls give better control
@wire provides cleaner reactive design
Proper state handling (loading, empty, error) is critical
UI should not depend on raw backend data → always transform


🚨 Common Mistakes Avoided
❌ Passing '$rating' in imperative call
❌ Using data variable for loading state
❌ Mixing UI states (loading vs empty vs data)
❌ No data transformation for UI styling


📸 UI Highlights


<img width="605" height="239" alt="1" src="https://github.com/user-attachments/assets/fcc2f01c-ae42-409e-9e29-1ed7f57bb768" />
<img width="299" height="221" alt="2" src="https://github.com/user-attachments/assets/8130d62e-f9ce-4a46-a116-be796a993ef6" />
<img width="298" height="227" alt="3" src="https://github.com/user-attachments/assets/9693ea5c-c076-416f-a6e9-7f795afe0eb4" />
<img width="299" height="224" alt="4" src="https://github.com/user-attachments/assets/941e6c15-257d-4795-979d-29aa4d074946" />
<img width="304" height="242" alt="5" src="https://github.com/user-attachments/assets/421d42c8-7149-4350-ab70-6dec2b7e22ed" />
<img width="299" height="244" alt="6" src="https://github.com/user-attachments/assets/81f2ba0d-d25b-4ec6-b8d1-d9d46ef0b34b" />

